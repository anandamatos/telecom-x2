# Challenge Telecom X: análise de evasão de clientes - Parte 2

## Importância do Desafio
======================

 [Próxima Atividade](https://cursos.alura.com.br/course/challenge-telecom-x/task/198444/next)

O **Desafio Telecom X parte 2** oferece uma oportunidade única para aplicar conhecimentos fundamentais de **estatística**, **regressão linear** e **machine learning**, além de habilidades essenciais de **ciência de dados**, em um cenário de negócios real.

Aplicação prática do conhecimento
---------------------------------

> Neste desafio, você colocará em prática **conceitos fundamentais de estatística**, essenciais para entender o comportamento dos dados e embasar decisões analíticas.

> Um dos principais passos será **preparar e separar os dados** de forma adequada para a criação de **modelos preditivos**, garantindo que haja equilíbrio entre os dados de treino e teste --- algo indispensável para a construção de modelos confiáveis.

> Ao realizar a **análise de correlação entre variáveis**, será possível identificar quais fatores mais influenciam o cancelamento de serviços (churn). Isso permitirá aplicar **regressão linear** como ferramenta para modelar essas relações e entender o impacto de cada variável no comportamento dos clientes.

> Com isso, você irá construir uma base sólida para o desenvolvimento de modelos de **machine learning** voltados à previsão de churn, ajudando a empresa a antecipar o risco de perda de clientes e tomar decisões estratégicas para reduzir esse impacto.

Este desafio não só contribui para o seu crescimento na área de Data Science, como também demonstra na prática como a **ciência de dados** pode ser usada para resolver problemas reais enfrentados por empresas no mercado.

## Preparando o ambiente
=====================

 [Próxima Atividade](https://cursos.alura.com.br/course/challenge-telecom-x/task/198446/next)

Criando modelos preditivos
==========================

Após concluir a etapa de **ETL (Extract, Transform, Load)** na Parte 1 do desafio, é hora de utilizar os dados já tratados para avançar na construção de **modelos preditivos**.

Para isso, certifique-se de estar utilizando o **conjunto de dados que você já limpou e transformou** anteriormente. Essa continuidade é fundamental para garantir a consistência das análises e a eficácia dos modelos.

Caso você ainda não tenha extraído os dados tratados da Parte 1, pode salvá-los em um arquivo CSV com o seguinte comando:

```
`
df.to_csv("dados_tratados.csv", index=False)
`Copiar código
```

Com esse arquivo, você poderá carregar os dados já prontos para análise e modelagem nesta segunda parte do desafio.

## Suba seu projeto no GitHub
==========================

 [Próxima Atividade](https://cursos.alura.com.br/course/challenge-telecom-x/task/198448/next)

Git e GitHub
============

> Git e GitHub são ferramentas essenciais para qualquer analista de dados, permitindo o versionamento e o compartilhamento eficiente dos projetos.

Neste desafio, você deverá **subir seu caderno do Colab para um repositório no GitHub**. Isso garantirá que seu progresso esteja salvo e acessível de qualquer lugar.

O que você precisa fazer:
-------------------------

1.  Crie um **novo repositório no GitHub** para armazenar seu projeto.

2.  Exporte seu caderno do Colab como um arquivo `.ipynb`.

3.  Faça o **upload** do caderno para o repositório.

4.  Mantenha seu trabalho atualizado utilizando os comandos `git pull`, `git add`, `git commit` e `git push` sempre que fizer alterações.

Caso precise relembrar conceitos, confira os recursos abaixo:

-   [Começando com Git: Aprendendo a versionar](https://www.alura.com.br/artigos/comecando-com-git-aprendendo-versionar)

-   [GitHub: diferentes maneiras de compartilhar seu projeto](https://cursos.alura.com.br/extra/alura-mais/github-diferentes-maneiras-de-compartilhar-seu-projeto-c2002)

-   [Como escrever um README incrível no seu GitHub](https://www.alura.com.br/artigos/escrever-bom-readme)

* * * *

README
======

> O `README` é essencial para documentar seu projeto, explicando sua finalidade, funcionalidades e instruções de uso.

Como **desafio adicional**, crie um `README.md` para seu projeto **Telecom X - Parte 2**, incluindo:

1.  **O propósito da análise realizada**, destacando o objetivo principal: prever o churn de clientes com base em variáveis relevantes.

2.  **Estrutura do projeto e organização dos arquivos**, como o notebook principal, os dados tratados em CSV e qualquer pasta de visualizações.

3.  **Descrição do processo de preparação dos dados**, incluindo:

    -   Classificação das variáveis em categóricas e numéricas.

    -   Etapas de normalização ou codificação.

    -   Separação dos dados em **conjuntos de treino e teste**.

    -   Justificativas para as escolhas feitas durante a modelagem.

4.  **Exemplos de gráficos e insights obtidos** durante a análise exploratória de dados (EDA).

5.  **Instruções para executar o notebook**, incluindo quais bibliotecas precisam ser instaladas e como carregar os dados tratados.

Esse README tornará seu projeto mais completo, organizado e fácil de entender, o que é um diferencial importante tanto em ambientes acadêmicos quanto profissionais.

# <div><br class="Apple-interchange-newline">💡 Sobre o Desafío 💡</div>

#### 💡 Sobre o Desafío 💡

### Descrição

### **Telecom X -- Parte 2: Prevendo Churn**

#### 📣 **História do Desafio**

Parabéns! 🎉 Você foi promovido após seu excelente desempenho na análise exploratória da evasão de clientes na Telecom X. Sua dedicação, clareza na comunicação dos dados e visão estratégica fizeram a diferença.

Agora, você foi convidado a integrar oficialmente a equipe de **Machine Learning** da empresa!

* * * *

#### 🎯 **Missão**

Sua nova missão é desenvolver **modelos preditivos** capazes de prever quais clientes têm maior chance de cancelar seus serviços.

A empresa quer antecipar o problema da evasão, e cabe a você construir um pipeline robusto para essa etapa inicial de modelagem.

* * * *

#### 🧠 **Objetivos do Desafio**

-   Preparar os dados para a modelagem (tratamento, encoding, normalização).

-   Realizar análise de correlação e seleção de variáveis.

-   Treinar **dois ou mais modelos de classificação**.

-   Avaliar o desempenho dos modelos com métricas.

-   Interpretar os resultados, incluindo a **importância das variáveis**.

-   Criar uma conclusão estratégica apontando os principais fatores que influenciam a evasão.

* * * *

#### 🧰 **O que você vai praticar**

✅ Pré-processamento de dados para Machine Learning

✅ Construção e avaliação de modelos preditivos

✅ Interpretação dos resultados e entrega de insights

✅ Comunicação técnica com foco estratégico

* * * *

#### 🚀 **Você agora é: Analista de Machine Learning Júnior**

A Telecom X está confiando na sua entrega para dar os próximos passos em direção a uma **solução de inteligência preditiva** eficaz. Boa sorte!

# <div><br class="Apple-interchange-newline">Crie seu repositório de projetos no GitHub</div>

#### Crie seu repositório de projetos no GitHub

### Descrição

No desenvolvimento de projetos, sabemos como é essencial organizar seu trabalho desde o início. Por isso, neste desafio, você deverá criar um repositório no GitHub para armazenar e versionar seu projeto.

Mesmo que você ainda não tenha desenvolvido nenhum código, o objetivo é que você crie uma estrutura inicial para o projeto. À medida que avançar, você poderá atualizar e adicionar arquivos ao repositório.

Materiais de Apoio
Se precisar de ajuda, confira os seguintes recursos:

-   [Git - Configuração Inicial do Git](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Configura%C3%A7%C3%A3o-Inicial-do-Git)

-   [Iniciando um repositório com Git | Alura](https://www.alura.com.br/artigos/iniciando-repositorio-git?srsltid=AfmBOorPwqQUhHG3A3VaTH5KtGJA10qcvMMpnYFDojw9lMSaS9natUVX)

Organizar seu projeto desde o início facilita o desenvolvimento e garante boas práticas no controle de versões! 🚀


# 🛠️ Preparação dos Dados
## <div><br class="Apple-interchange-newline">Extração do Arquivo Tratado</div>

#### Extração do Arquivo Tratado

### Descrição

Carregue o arquivo CSV que contém os dados tratados anteriormente.

📂 **Atenção:** Utilize o mesmo arquivo que você limpou e organizou na **parte 1 do desafio Telecom X**. Ele deve conter somente as colunas relevantes, já com os dados corrigidos e padronizados.

## <div><br class="Apple-interchange-newline">Remoção de Colunas Irrelevantes</div>

#### Remoção de Colunas Irrelevantes

### Descrição

Elimine colunas que **não trazem valor para a análise** ou para **os modelos preditivos**, como identificadores únicos (por exemplo, o ID do cliente). Essas colunas não ajudam na previsão da evasão e podem até prejudicar o desempenho dos modelos.

## <div><br class="Apple-interchange-newline">Encoding</div>

#### Encoding

### Descrição

Transforme as variáveis categóricas em formato numérico para torná-las compatíveis com algoritmos de machine learning. Utilize um método de codificação adequado, como o **one-hot encoding**.

**Dicas:**

-   [get\_dummies vs OneHotEncoder: qual método escolher? | Alura](https://www.alura.com.br/artigos/get-dummies-vs-onehotencoder-qual-metodo-escolher?utm_term=&utm_campaign=topo-aon-search-gg-dsa-artigos_conteudos&utm_source=google&utm_medium=cpc&campaign_id=11384329873_164212380672_703829166693&utm_id=11384329873_164212380672_703829166693&hsa_acc=7964138385&hsa_cam=topo-aon-search-gg-dsa-artigos_conteudos&hsa_grp=164212380672&hsa_ad=703829166693&hsa_src=g&hsa_tgt=aud-527303763294:dsa-425656816943&hsa_kw=&hsa_mt=&hsa_net=google&hsa_ver=3&gad_source=1&gad_campaignid=11384329873&gclid=CjwKCAjwz_bABhAGEiwAm-P8YcX5MR72F94-IuQpgazH03079qa2AYVScM4YseUiH-6yqcctRGwHuRoCLq4QAvD_BwE)
-   
## <div><br class="Apple-interchange-newline">Verificação da Proporção de Evasão</div>

#### Verificação da Proporção de Evasão

### Descrição

Calcule a proporção de clientes que evadiram em relação aos que permaneceram ativos. Avalie se há desequilíbrio entre as classes, o que pode impactar modelos preditivos e a análise de resultados.

**Dicas:**

-   [pandas.DataFrame.value\_counts --- pandas 2.3.1 documentation](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.value_counts.html)
-   
## <div><br class="Apple-interchange-newline">Balanceamento de Classes (opcional )</div>

#### Balanceamento de Classes (opcional )

### Descrição

Caso queira aprofundar a análise, aplique técnicas de balanceamento como *undersampling* ou *oversampling*. Em situações de forte desbalanceamento, ferramentas como o **SMOTE** podem ser úteis para gerar exemplos sintéticos da classe minoritária.

**Dicas:**

-   [Lidando com o desbalanceamento de dados | Alura](https://www.alura.com.br/artigos/lidando-com-desbalanceamento-dados?srsltid=AfmBOopTgyC_tpujwkC778gYjcLituqgxknih2Cr4vD72_OFHSB4v35M)
-   
## <div><br class="Apple-interchange-newline">Normalização ou Padronização (se necessário)</div>

#### Normalização ou Padronização (se necessário)

### Descrição

Avalie a necessidade de normalizar ou padronizar os dados, conforme os modelos que serão aplicados.
Modelos baseados em distância, como **KNN**, **SVM**, **Regressão Logística** e **Redes Neurais**, requerem esse pré-processamento.
Já modelos baseados em árvore, como **Decision Tree**, **Random Forest** e **XGBoost**, não são sensíveis à escala dos dados.

**Dicas:**

-   [A importância da normalização e padronização dos dados em Machine Learning](https://medium.com/ipnet-growth-partner/padronizacao-normalizacao-dados-machine-learning-f8f29246c12)


# 🎯 Correlação e Seleção de Variáveis
## <div><br class="Apple-interchange-newline">Análise de Correlação</div>

#### Análise de Correlação

### Descrição

Visualize a matriz de correlação para identificar relações entre variáveis numéricas. Observe especialmente **quais variáveis apresentam maior correlação com a evasão**, pois elas podem ser fortes candidatas para o modelo preditivo.

## <div><br class="Apple-interchange-newline">Análises Direcionadas</div>

#### Análises Direcionadas

### Descrição

Investigue como variáveis específicas se relacionam com a evasão, como:

-   **Tempo de contrato × Evasão**

-   **Total gasto × Evasão**

Utilize gráficos como **boxplots** ou **dispersão (scatter plots)** para visualizar padrões e possíveis tendências.

# 🤖 Modelagem Preditiva

## <div><br class="Apple-interchange-newline">Separação de Dados</div>

#### Separação de Dados

### Descrição

Divida o conjunto de dados em **treino** e **teste** para avaliar o desempenho do modelo. Uma divisão comum é **70% para treino** e **30% para teste**, ou **80/20**, dependendo do tamanho da base de dados.

## <div><br class="Apple-interchange-newline">Criação de Modelos</div>

#### Criação de Modelos

### Descrição

Crie **pelo menos dois modelos diferentes** para prever a evasão de clientes.

-   Um modelo pode **exigir normalização**, como **Regressão Logística** ou **KNN**.

-   O outro modelo pode **não exigir normalização**, como **Árvore de Decisão** ou **Random Forest**.

> 💡 A escolha de aplicar ou não a normalização depende dos modelos selecionados. Ambos os modelos podem ser criados sem normalização, mas a combinação de modelos com e sem normalização também é uma opção.

Justifique a escolha de cada modelo e, se optar por normalizar os dados, explique a necessidade dessa etapa.

# 📋  Interpretação e Conclusões

## <div><br class="Apple-interchange-newline">Análise de Importância das Variáveis</div>

#### Análise de Importância das Variáveis

### Descrição

Após escolher os modelos, realize a análise das variáveis mais relevantes para a previsão de evasão:

-   **Regressão Logística**: investigue os **coeficientes** das variáveis, que mostram sua contribuição para a previsão de evasão.

-   **KNN (K-Nearest Neighbors)**: Observe como os **vizinhos mais próximos** influenciam a decisão de classificação. As variáveis mais impactantes podem ser aquelas que mais contribuem para a proximidade entre os pontos de dados.

-   **Random Forest**: Utilize a **importância das variáveis** fornecida pelo modelo. O Random Forest calcula a importância com base em como cada variável contribui para a redução da impureza durante as divisões das árvores.

-   **SVM (Support Vector Machine)**: No SVM, as variáveis mais relevantes são aquelas que influenciam a **fronteira de decisão** entre as classes. Você pode analisar os **coeficientes dos vetores de suporte** para entender quais variáveis têm maior impacto.

-   **Outros Modelos**: Dependendo do modelo escolhido, considere a análise de métricas específicas para entender a relevância das variáveis. Por exemplo, **coeficientes** em modelos lineares, **pesos** em redes neurais, ou **importância relativa** em boosting (como XGBoost).


## <div><br class="Apple-interchange-newline">Conclusão</div>

#### Conclusão

### Descrição

Elaborem um relatório detalhado, destacando os fatores que mais influenciam a evasão, com base nas variáveis selecionadas e no desempenho de cada modelo.

-   Identifiquem os **principais fatores** que afetam a evasão de clientes e proponham estratégias de retenção com base nos resultados obtidos.