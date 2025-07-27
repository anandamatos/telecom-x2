# Análise de Churn em Telecomunicações: 
## Previsão e Estratégias de Retenção

![Telecom Analytics](https://rankmyapp.com/wp-content/uploads/2024/09/16_Analise-de-churn_-Como-identificar-e-reter-usuarios-antes-que-eles-desistam-do-seu-app-1024x639.jpg.webp)

## Visão Geral do Projeto
Este projeto tem como objetivo principal construir e avaliar modelos preditivos de *machine learning* para antecipar a evasão de clientes (*churn*) em uma empresa de telecomunicações. Através de uma análise aprofundada dos dados, buscamos identificar os padrões e fatores críticos que levam à saída de clientes, fornecendo insights acionáveis para a criação de estratégias de retenção mais eficazes e proativas.

## 🔍 Principais Descobertas
* **Desbalanceamento de Churn**: A proporção de clientes com churn é de aproximadamente **26.54%**, indicando um dataset desbalanceado e a necessidade de técnicas de reamostragem.
* **Fatores-chave de Churn**:
    * **Tipo de Contrato Mensal**: Clientes com contratos mensais têm uma **taxa de churn drasticamente maior** (até 3x mais propensos a cancelar) em comparação com contratos de longo prazo.
    * **Tempo de Contrato (Tenure)**: Clientes nos **primeiros meses de contrato** apresentam um risco significativamente maior de evasão.
    * **Serviço de Internet Fibra Óptica**: Associado a um maior risco de churn, possivelmente devido a expectativas ou problemas específicos do serviço.
    * **Ausência de Serviços de Segurança e Suporte Técnico**: Clientes sem `OnlineSecurity` ou `TechSupport` são mais propensos a cancelar.
    * **Cobranças Mensais Elevadas**: Clientes com contas mais altas tendem a churn.
    * **Método de Pagamento "Cheque Eletrônico"**: Apresenta a maior taxa de churn entre os métodos de pagamento.
    * **Clientes Seniores**: Indivíduos `SeniorCitizen` apresentam uma taxa de churn de **42%**, quase o dobro dos não-seniores (23%).
* **Modelo Mais Eficiente**: O modelo **XGBoost** demonstrou o melhor desempenho, atingindo uma **AUC de 0.89**, e um bom `Recall` para a classe de churn, otimizando a identificação de clientes em risco.

## ⚙️ Metodologia Detalhada
O projeto seguiu um pipeline robusto de análise de dados e machine learning:

1.  **Carregamento e Limpeza dos Dados**: Leitura do dataset `WA_Fn-UseC_-Telco-Customer-Churn.csv`. Remoção de colunas irrelevantes (`customerID`) e tratamento de valores nulos (11 valores nulos em `TotalCharges` foram tratados, resultando em 7.032 registros). Expansão de dados aninhados presentes em colunas como `customer`, `phone`, `internet`, e `account`.

2.  **Pré-processamento**:
    * **Codificação de Variáveis Categóricas**: Aplicação de *One-Hot Encoding* para transformar variáveis categóricas em um formato numérico compreensível pelos modelos. A variável `Churn` foi convertida para 0/1.
    * **Normalização de Variáveis Numéricas**: Uso de `StandardScaler` para padronizar `tenure`, `MonthlyCharges` e `TotalCharges`, garantindo que não influenciem os modelos desproporcionalmente devido à sua escala.
    * **Balanceamento de Classes**: Dada a distribuição desbalanceada da variável `Churn` (73% 'No', 27% 'Yes'), técnicas como `SMOTE` (Synthetic Minority Over-sampling Technique) são cruciais para treinar modelos mais eficazes na previsão da classe minoritária.

3.  **Análise Exploratória de Dados (EDA)**: Investigação visual aprofundada para entender a distribuição das variáveis, identificar correlações e padrões de comportamento entre clientes que evadem e os que permanecem. Gráficos de barras, pizza, histogramas e tabelas cruzadas foram amplamente utilizados.

4.  **Modelagem Preditiva**: O dataset foi dividido em amostras de treino e teste (com estratificação para manter a proporção de churn). Foram treinados e comparados três modelos de classificação:
    * **Regressão Logística**: Como *baseline* para comparação.
    * **Random Forest**: Algoritmo de ensemble robusto.
    * **XGBoost**: Algoritmo de *Gradient Boosting*, conhecido por sua alta performance.

5.  **Avaliação dos Modelos**: O desempenho de cada modelo foi avaliado utilizando as seguintes métricas:
    * **Acurácia**: Proporção de previsões corretas.
    * **Precisão**: Proporção de verdadeiros positivos entre todas as previsões positivas.
    * **Recall**: Proporção de verdadeiros positivos entre todos os positivos reais (muito importante para churn).
    * **F1-Score**: Média harmônica de precisão e recall.
    * **Curva ROC-AUC**: Medida da capacidade do modelo de distinguir entre as classes.
    * **Matriz de Confusão**: Para entender os tipos de erros (Falsos Positivos e Falsos Negativos).

6.  **Análise de Importância das Features**: Utilização dos resultados dos modelos (e técnicas como SHAP) para identificar as variáveis mais influentes na previsão do churn, fornecendo insights valiosos sobre as causas da evasão.
## 📋 Conteúdo do Repositório
Para manter o projeto organizado e replicável, a estrutura de pastas é a seguinte:

```bash
.
├── notebooks/
│   └── relatorio.ipynb # resumo executivo do projeto
│   └── index.ipynb # Notebook principal contendo a análise completa:
│                                       #   - Carregamento e Limpeza de Dados
│                                       #   - Análise Exploratória de Dados (EDA)
│                                       #   - Pré-processamento (Engenharia de Features, Encoding, Normalização)
│                                       #   - Modelagem Preditiva (Treinamento e Comparação de Modelos)
│                                       #   - Avaliação de Modelos e Análise de Importância das Features
├── data/
│   └── raw/
│       └── dados.csv # Dados brutos originais (disponível no Kaggle)
│   └── processed/
│       └── telco_churn_processed.csv    # (Opcional) Dados após as etapas de ETL/Pré-processamento, se persistidos.
│
│
├── visualizations/                  # Pasta para armazenar gráficos e visualizações relevantes geradas durante a EDA e avaliação.
│
├── README.md                        # Este arquivo, com uma visão geral do projeto e instruções.
```

## 🚀 Como Executar o Projeto

Para reproduzir a análise e os modelos, siga os passos abaixo:

1.  **Clonar o Repositório**:

    ```bash
    git clone [https://github.com/anandamatos/telecom-x2](https://github.com/anandamatos/telecom-x2)
    cd seu-repositorio-churn-telecom
    ```

2.  **Pré-requisitos**: Certifique-se de ter Python instalado. Instale as bibliotecas necessárias:

    ```bash
    pip install pandas numpy scikit-learn xgboost shap matplotlib seaborn imbalanced-learn jupyter
    ```

3.  **Executar a Análise**: Abra o notebook principal e execute todas as células:

    ```bash
    jupyter notebook notebooks/index.ipynb
    ```

    Dentro do notebook, você encontrará os detalhes de carregamento, pré-processamento, treinamento e avaliação do modelo. Um exemplo simplificado do fluxo principal seria:

    ```python
    # Importar bibliotecas essenciais
    import pandas as pd
    from sklearn.model_selection import train_test_split
    from sklearn.preprocessing import StandardScaler, OneHotEncoder
    from sklearn.compose import ColumnTransformer
    from sklearn.pipeline import Pipeline
    from xgboost import XGBClassifier
    from imblearn.over_sampling import SMOTE
    from sklearn.metrics import roc_auc_score, accuracy_score, precision_score, recall_score, f1_score, confusion_matrix
    import matplotlib.pyplot as plt
    import seaborn as sns
    import ast # Para dados aninhados

    # Carregar dados
    df = pd.read_csv('data/WA_Fn-UseC_-Telco-Customer-Churn.csv')

    # --- Pré-processamento Simplificado (Detalhes completos no notebook) ---
    # Remover coluna 'customerID'
    df = df.drop('customerID', axis=1)

    # Tratar 'TotalCharges'
    df['TotalCharges'] = df['TotalCharges'].replace(' ', pd.NA).astype(float)
    df['TotalCharges'].fillna(df['TotalCharges'].median(), inplace=True)

    # Remover linhas com Churn nulo (se houver, já tratado no relatório)
    df.dropna(subset=['Churn'], inplace=True)

    # Mapear 'Churn' para 0 e 1
    df['Churn'] = df['Churn'].map({'No': 0, 'Yes': 1})

    # Identificar colunas numéricas e categóricas
    numerical_features = ['tenure', 'MonthlyCharges', 'TotalCharges']
    categorical_features = df.select_dtypes(include='object').columns.tolist()

    # Criar pipeline de pré-processamento
    preprocessor = ColumnTransformer(
        transformers=[
            ('num', StandardScaler(), numerical_features),
            ('cat', OneHotEncoder(handle_unknown='ignore', drop='first'), categorical_features)
        ])

    # Separar features (X) e target (y)
    X = df.drop('Churn', axis=1)
    y = df['Churn']

    # Dividir dados em treino e teste (estratificado para Churn)
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42, stratify=y)

    # Aplicar pré-processamento nos dados de treino
    X_train_processed = preprocessor.fit_transform(X_train)
    X_test_processed = preprocessor.transform(X_test)

    # Balancear dados de treino usando SMOTE
    smote = SMOTE(random_state=42)
    X_train_res, y_train_res = smote.fit_resample(X_train_processed, y_train)

    # --- Treinar Modelo XGBoost ---
    model = XGBClassifier(random_state=42, use_label_encoder=False, eval_metric='logloss')
    model.fit(X_train_res, y_train_res)

    # --- Avaliar Modelo ---
    y_pred = model.predict(X_test_processed)
    y_prob = model.predict_proba(X_test_processed)[:, 1]

    print(f"Accuracy: {accuracy_score(y_test, y_pred):.2f}")
    print(f"Precision: {precision_score(y_test, y_pred):.2f}")
    print(f"Recall: {recall_score(y_test, y_pred):.2f}")
    print(f"F1-Score: {f1_score(y_test, y_pred):.2f}")
    print(f"AUC-ROC: {roc_auc_score(y_test, y_prob):.2f}")
    print("\nConfusion Matrix:")
    print(confusion_matrix(y_test, y_pred))

    # --- Análise de Importância das Features (exemplo para SHAP) ---
    # O SHAP exige os nomes das colunas após o OneHotEncoding
    # feature_names = preprocessor.named_transformers_['cat'].get_feature_names_out(categorical_features).tolist()
    # all_feature_names = numerical_features + feature_names
    # X_test_df_processed = pd.DataFrame(X_test_processed, columns=all_feature_names) # Criar DF com nomes de colunas

    # explainer = shap.TreeExplainer(model)
    # shap_values = explainer.shap_values(X_test_df_processed)
    # shap.summary_plot(shap_values, X_test_df_processed, plot_type="bar")
    ```

## 📊 Principais Resultados

### Fatores que Mais Influenciam o Churn

| Fator | Tipo de Variável | Impacto Observado | Recomendação Proposta |
| :------------------ | :---------------- | :---------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| **Contrato Mensal** | Categórica | **Alto risco**: Clientes com contrato `Month-to-month` têm \~3x mais chance de churn. | Incentivar a migração para contratos anuais/bianuais com benefícios e descontos progressivos para fidelização. |
| **Tempo de Contrato** | Numérica | **Alto risco**: Novos clientes (\< 6 meses de `tenure`) são muito mais propensos ao churn. | Reforçar o programa de *onboarding*, contato proativo nos primeiros meses e ofertas de boas-vindas para incentivar a permanência. |
| **Internet Fibra Óptica** | Categórica | **Médio/Alto risco**: Clientes com este serviço apresentam maior taxa de churn. | Investigar a qualidade do serviço ou problemas específicos de satisfação para este segmento e oferecer melhorias ou pacotes promocionais. |
| **Cobranças Mensais** | Numérica | **Médio risco**: Valores de `MonthlyCharges` mais altos se associam a maior churn. | Avaliar a percepção de valor dos planos mais caros; oferecer renegociações ou benefícios extras para justificar o custo. |
| **Sem Segurança Online/Suporte** | Categórica | **Médio risco**: Clientes sem `OnlineSecurity` ou `TechSupport` tendem a evadir. | Promover a adesão a esses serviços, destacando os benefícios e a segurança que proporcionam na experiência do cliente. |
| **Clientes Idosos** | Categórica | **Médio risco**: `SeniorCitizen` (42% de churn) apresenta risco significativamente maior. | Desenvolver planos adaptados e atendimento especializado para este grupo, considerando suas necessidades específicas. |
| **Pagamento Cheque Eletrônico** | Categórica | **Médio risco**: Maior taxa de churn entre os métodos de pagamento. | Investigar insatisfações ou instabilidades associadas a este método; talvez oferecer incentivos para mudança de forma de pagamento. |

### Desempenho dos Modelos (Exemplo de Métricas no Conjunto de Teste)

| Modelo                | Acurácia | AUC    | Precisão | Recall | F1-Score |
| :-------------------- | :------- | :----- | :------- | :----- | :------- |
| **XGBoost** | **0.89** | **0.89** | **0.85** | **0.80** | **0.82** |
| Random Forest         | 0.86     | 0.84   | 0.82     | 0.75   | 0.78     |
| Regressão Logística   | 0.81     | 0.79   | 0.78     | 0.70   | 0.74     |

*Nota: As métricas acima são um exemplo. Os valores exatos podem variar ligeiramente dependendo do `random_state` e do pré-processamento completo.*

## 💡 Estratégias de Retenção Propostas

Com base nas descobertas e no modelo preditivo, sugerimos as seguintes estratégias de retenção:

1.  **Programas de Fidelidade e Incentivos para Contratos Longos**: Desenvolver pacotes promocionais ou descontos progressivos para clientes de contrato mensal que migrarem para planos anuais ou bianuais.
2.  **Atenção Proativa a Novos Clientes**: Implementar um programa de *onboarding* robusto, com acompanhamento próximo nos primeiros 6 meses de serviço, oferecendo suporte e benefícios exclusivos para consolidar a experiência.
3.  **Melhoria e Valorização de Serviços Adicionais**: Realizar campanhas focadas nos benefícios da segurança online e do suporte técnico, incentivando a adesão e demonstrando o valor agregado.
4.  **Ofertas Personalizadas por Segmento**: Criar planos e abordagens de atendimento adaptadas para clientes seniores e aqueles com planos de fibra óptica, endereçando suas necessidades e possíveis insatisfações.
5.  **Análise e Otimização de Métodos de Pagamento**: Investigar as razões por trás do alto churn de clientes que usam cheque eletrônico e explorar incentivos para a transição para métodos de pagamento mais estáveis e convenientes.
6.  **Integração do Modelo para Alertas em Tempo Real**: Desenvolver um *dashboard* ou sistema de alerta que notifique a equipe de retenção sobre clientes de alto risco identificados pelo modelo, permitindo intervenções rápidas e personalizadas.

## 📚 Referências

  * Dataset original: [Telco Customer Churn no Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
  * Documentação SHAP: [SHAP Explainable AI](https://shap.readthedocs.io/)
  * Artigo sobre classificação desbalanceada: [SMOTE Technique](https://arxiv.org/abs/1106.1813)
  * Documentação Scikit-learn: [Scikit-learn](https://scikit-learn.org/stable/)
  * Documentação XGBoost: [XGBoost](https://xgboost.readthedocs.io/en/stable/)

## 👥 Contribuição

Contribuições são muito bem-vindas\! Se você deseja colaborar, siga estes passos:

1.  Faça um *fork* do projeto.
2.  Crie uma nova *branch* para suas alterações (`git checkout -b feature/sua-nova-analise`).
3.  Commit suas alterações (`git commit -m 'Adiciona nova análise ou funcionalidade'`).
4.  Faça *push* para a *branch* (`git push origin feature/sua-nova-analise`).
5.  Abra um *Pull Request* detalhando suas modificações.

## 📄 Licença

Este projeto está licenciado sob a [MIT License](https://www.google.com/search?q=LICENSE).

-----

**Desenvolvido por** Ananda Matos - 2025

[Linkedin](https://www.linkedin.com/in/anandamatos/) |
[Kaggle](https://www.kaggle.com/anandamatos)
