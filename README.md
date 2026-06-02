# Capacitação Asimov
### Semana 4
>Italo - Rodrigo

# Análise Exploratória e Estatística — Students Performance

Este notebook consolida dois trabalhos de análise de dados realizados sobre a base **StudentsPerformance.csv**.  
A proposta é organizar as contribuições dos estudantes em um único relatório, mantendo as análises mais relevantes.

## Objetivos da análise

- Carregar, organizar e compreender a estrutura da base de dados;
- Verificar qualidade dos dados, valores ausentes e duplicidades;
- Analisar a distribuição das variáveis categóricas;
- Comparar o desempenho dos alunos nas notas de Matemática, Leitura e Escrita;
- Investigar relações entre desempenho e variáveis como gênero, almoço, curso de preparação, escolaridade familiar e raça/etnia;
- Aplicar estatísticas descritivas e testes inferenciais;
- Produzir visualizações gráficas úteis para apresentação acadêmica.

## 1. Importação das bibliotecas

As importações foram reunidas em uma única célula para evitar duplicidade.  
Foram mantidas as bibliotecas usadas nos dois trabalhos: `pandas`, `numpy`, `matplotlib`, `seaborn` e funções estatísticas do `scipy`.

## 2. Carregamento da base de dados

A base utilizada é o arquivo `StudentsPerformance.csv`.  
Para executar o notebook sem erro, mantenha esse arquivo na mesma pasta do notebook.

## 3. Pré-processamento e padronização dos dados

Nesta etapa, os nomes das colunas foram traduzidos para português, seguindo a lógica presente nos trabalhos.  
Também foi criada a coluna `media geral`, que representa a média das três notas de cada aluno.

## 4. Verificação da qualidade da base

Aqui verificamos tipos de dados, valores nulos e linhas duplicadas.  
Essa etapa consolida a análise inicial feita nos dois arquivos.

## 5. Descrição da base de dados

A base possui variáveis categóricas relacionadas ao perfil dos alunos e variáveis numéricas relacionadas ao desempenho em provas.

- **Variáveis categóricas:** gênero, raça/etnia, nível de educação familiar, tipo de almoço e curso de preparação.
- **Variáveis numéricas:** nota em Matemática, nota em Leitura, nota em Escrita e média geral.

## 6. Análise exploratória das variáveis categóricas

Os gráficos abaixo mostram a distribuição dos principais grupos presentes na base.  
Foram mantidas as visualizações de distribuição por gênero, raça/etnia, educação familiar, almoço e curso de preparação.

## 7. Estatísticas descritivas das notas

Esta seção reúne médias, medianas, quartis, desvio padrão e outras medidas para as três notas e para a média geral.
### Interpretação inicial

As medidas de centralidade mostram o desempenho típico dos alunos em cada área avaliada.  
O desvio padrão indica o quanto as notas variam em relação à média: quanto maior o desvio padrão, maior a dispersão das notas.

## 8. Distribuição das notas e boxplots

Os histogramas ajudam a observar o formato da distribuição das notas.  
Os boxplots permitem comparar mediana, amplitude interquartil e possíveis outliers.

## 9. Análise de quartis e outliers da média geral

Esta etapa preserva a lógica do primeiro trabalho para identificar limites pelo método do intervalo interquartil.

## 10. Correlação entre as notas

Esta análise mostra se alunos com bom desempenho em uma prova também tendem a ter bom desempenho nas outras.

## 11. Médias das notas por grupos

Esta seção consolida as comparações feitas por gênero, almoço, curso de preparação, nível de educação familiar e raça/etnia.

## 12. Visualização das médias por grupos

Foram mantidos gráficos que complementam a leitura das tabelas, priorizando a comparação da `media geral` para evitar excesso de visualizações repetidas.

## 13. Boxplots com intervalo de confiança da média

O segundo trabalho trouxe uma boa ideia de combinar boxplot com intervalo de confiança de 95%.  
Abaixo, essa ideia foi reorganizada em uma função para evitar repetição de código.

## 14. Relações entre variáveis categóricas e desempenho

Aqui foram preservadas as comparações cruzadas do segundo trabalho, mas compactadas para reduzir repetição.  
O foco passa a ser a `media geral`, em vez de repetir o mesmo conjunto de gráficos para Matemática, Leitura e Escrita separadamente.

## 15. Testes de normalidade das notas

Foram mantidos os histogramas, gráficos Q-Q e testes de Shapiro presentes no segundo trabalho.  
Como a base possui 1000 linhas, o teste de Shapiro pode ser sensível: valores de p muito baixos não impedem a análise, mas indicam desvio da normalidade perfeita.

## 16. Probabilidades aproximadas por faixas de quartis

Esta parte preserva a ideia do segundo trabalho de usar a distribuição normal para estimar probabilidades entre faixas de quartis.  
A interpretação deve ser feita como aproximação estatística.

## 17. Testes estatísticos inferenciais

Nesta etapa foram reunidos os testes estatísticos complementares dos trabalhos:

- **Teste t de Student:** compara a média geral entre alunos que completaram e não completaram o curso de preparação.
- **ANOVA:** verifica se há diferença significativa de média geral entre níveis de educação familiar.
- **Qui-quadrado:** verifica associação entre variáveis categóricas.

## 18. Principais descobertas

Com base nas análises realizadas, podemos destacar:

1. A base possui 1000 registros e 8 colunas originais, além da coluna criada `media geral`.
2. A maior parte dos alunos não realizou curso de preparação.
3. Alunos que completaram o curso de preparação apresentaram desempenho médio superior.
4. A variável `almoco` também apresenta diferença relevante nas médias, com maior desempenho médio para alunos com almoço `standard`.
5. As notas de Leitura e Escrita apresentaram correlação muito forte.
6. O grupo `female` teve maiores médias em Leitura e Escrita, enquanto o grupo `male` teve maior média em Matemática.
7. Níveis mais altos de educação familiar aparecem associados a médias gerais mais altas.
8. As análises inferenciais indicam que algumas diferenças observadas entre grupos são estatisticamente relevantes.
