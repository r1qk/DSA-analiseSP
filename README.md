# Projeto Data Science and Analytics - FIAP

### Integrantes

Felipe Souza Carvalho  
Gustavo Hackime Costa  
Luiz Henrique Macedo Graça  
Riquelme Santos da Mata

# Tema) Segurança pública: evolução dos indicadores de criminalidade entre 2023 e 2025.

## Definição

A segurança pública é um tema de grande relevância para a sociedade, uma vez
que a ocorrência de crimes afeta diretamente a qualidade de vida da população e demanda
ações contínuas do poder público.

## Objetivo

Analisar a evolução dos registros de diferentes naturezas criminais entre os anos de
2023 e 2025, considerando dados mensais de sete regiões: Arujá, Barueri, Caieiras,
Guararema, Guarulhos, Itaquaquecetuba, São Bernardo do Campo e Suzano.

A análise busca identificar quais tipos de crimes apresentaram redução, estabilidade
ou aumento ao longo do período, bem como identificar como os indicadores de
criminalidade evoluíram entre o período e as regiões.

## Perguntas

A partir da definição formada e o objetivo definido, as seguintes perguntas foram
formuladas para análise:

#### “Houve redução, estabilidade ou aumento nos indicadores

criminais?”
Esta pergunta busca identificar a evolução geral temporal dos registros criminais.

#### “Quais naturezas criminais apresentaram as maiores variações?”

A finalidade desta questão é identificar quais categorias tiveram maior redução ou
crescimento.

#### “Existem períodos do ano em que determinados tipos de crimeapresentam maior concentração de ocorrências?”

A análise mensal permite identificar possíveis padrões sazonais ou períodos de maior
ocorrência.

## Descrição do dataset

O dataset utilizado apresenta os registros de ocorrências criminais organizados por
natureza do crime e mês, contendo também o total de ocorrências no período.
Os dados são disponibilizados para diferentes regiões e anos, permitindo a análise
da evolução temporal e a comparação entre localidades.
A estrutura básica dos dados é composta pelas seguintes variáveis:

- Natureza:
  - Tipo ou categoria da ocorrência criminal;

- Janeiro – Dezembro:
  - Número de ocorrências registradas no respectivo mês, de Janeiro a Dezembro;
- Total:
  - Soma das ocorrências registradas nos 12 meses do respectivo ano. Além disso, os dados foram limitados aos seguintes municípios: Arujá, Barueri, Caieiras, Guararema, Guarulhos, Itaquaquecetuba, São Bernardo do Campo e Suzano. Não somente, o período de tempo foi limitado para os anos de 2023, 2024 e 2025.

Também foi feito um agrupamento das diversas naturezas criminais para facilitar a
análise. As seguintes categorias foram criadas:

- Crimes contra a vida
  - Homicídio doloso;
  - Nº de vítimas em homicídio doloso;
  - Homicídio doloso por acidente de trânsito;
  - Nº de vítimas em homicídio doloso por acidente de trânsito;
  - Homicídio culposo por acidente de trânsito;
  - Homicídio culposo (outros);
  - Tentativa de homicídio;
  - Lesão corporal seguida de morte;
  - Latrocínio;
  - Nº de vítimas em latrocínio.

- Lesões corporais
  - Lesão corporal dolosa;
  - Lesão corporal culposa por acidente de trânsito;
  - Lesão corporal culposa (outros).

- Crimes sexuais
  - Total de estupro;
  - Estupro;
  - Estupro de vulnerável.

- Crimes patrimoniais
  - Total de roubos (outros);
  - Roubo (outros);
  - Roubo de veículo;
  - Roubo a banco;
  - Roubo de carga;
  - Furto (outros);
  - Furto de veículo.

Categorias que representam dados duplicados, como “Total de estupro” e “Estupro”
foram levadas em consideração e tratadas devidamente na análise exploratória.

## Análise exploratória dos dados

Inicialmente serão analisados o volume total de ocorrências por ano, a distribuição
das ocorrências por natureza, evolução mensal das principais categorias e a variação dos
registros entre 2023, 2024 e 2025.

### Volume de ocorrências por ano

Gráfico 01 – Total de ocorrências registradas por ano

<img src="imgs\grafico1.png" alt="Gráfico de volume de ocorrencias por ano" width="500">

O volume total ficou estável entre 2023 e 2024, uma variação de menos de 0,3%. Já
entre 2024 e 2025 houve uma queda mais perceptível, de cerca de 3,8%. Em todo o
período, a redução foi de aproximadamente 3,6%, sugerindo uma leve tendência de queda
concentrada no último ano analisado, não um declínio constante ao longo dos três anos.

### Principais naturezas criminais

Gráfico 02 – Distribuição das ocorrências por natureza

<img src="imgs\grafico2.png" alt="Gráfico de volume de ocorrencias por ano" width="500">

Crimes patrimoniais dominam disparadamente o total (176.480 ocorrências),
respondendo por mais da metade de tudo que foi registrado, bem à frente de Lesões
corporais (44.200). Crimes sexuais (2.954) e Crimes contra a vida (1.882) aparecem com
volumes muito menores, o que é esperado dado que homicídio e crimes sexuais tendem a
ser numericamente mais raros que roubo/furto, mesmo sendo mais graves.
Isso sugere que, ao interpretar o indicador geral de criminalidade, vale sempre
separar por categoria, pois um KPI agregado tende a ser dominado pelo comportamento de
Crimes patrimoniais, escondendo tendências das outras categorias.

### Distribuição de ocorrências nos meses

Gráfico 03 – Desvio-padrão de ocorrências em cada mês

<img src="imgs\grafico3.png" alt="Gráfico de volume de ocorrencias por ano" width="500">

Os valores de desvio-padrão ficam bastante próximos entre si ao longo dos 12
meses, variando num intervalo estreito de aproximadamente 129,7 (Junho) a 145,9
(Outubro), uma diferença de cerca de 12%. Isso indica que não há um padrão sazonal forte
de dispersão: a variabilidade entre naturezas/cidades não muda muito dependendo da
época do ano.
Outubro se destaca como o mês de maior dispersão (145,9), enquanto Junho e
Fevereiro têm os valores mais baixos (por volta de 129–130), mas, dado o quão próximos
todos os valores estão, essa diferença provavelmente reflete mais ruído normal do que um
evento sazonal identificável.

### Evolução dos principais indicadores

Gráfico 04 – Evolução dos registros entre 2023 e 2025

<img src="imgs\grafico4.png" alt="Gráfico de volume de ocorrencias por ano" width="500">

Crimes patrimoniais seguem sendo, disparadamente, a categoria dominante, mas
com queda consistente ano a ano: de 60.755 (2023) para 59.771 (2024) e 55.954 (2025),
uma redução acumulada de aproximadamente 7,9% no período, concentrada
principalmente entre 2024 e 2025 (-6,4%).
Lesões corporais têm trajetória oposta: cresce de forma constante, de 13.645 (2023)
para 14.776 (2024) e 15.779 (2025), um aumento acumulado de cerca de 15,6% no
período, o crescimento mais consistente entre as quatro categorias.
Crimes sexuais oscila sem tendência clara (986 → 1.018 → 950), enquanto Crimes
contra a vida se mantém praticamente estável ao longo dos três anos (628 → 622 → 632),
com variações pequenas o suficiente para serem consideradas ruído estatístico em vez de
tendência real.

## KPIs

A partir das perguntas definidas, foram selecionados os seguintes indicadores:

- Variação percentual
  - Permite medir a mudança relativa no período.
- Tendência mensal
  - Permite identificar crescimento ou redução ao longo do tempo.
- Variação por natureza
  - Identifica os crimes com maior mudança.
- Média mensal
  - Permite comparar o comportamento médio dos anos.
- Desvio-padrão mensal
  - Mede a dispersão das ocorrências.

As variações percentuais permitem comparar a evolução dos registros
independentemente do volume inicial, já que uma redução hipotética de 20 ocorrências
pode representar uma mudança muito diferente em uma região hipotética que possua 30
ocorrências com outra que tinha 500.

Além disso, o uso dos dados mensais permite analisar todo o período de 36 meses
estudado, em vez de somente considerar três observações anuais. Isso permite verificar se
existem tendências consistentes ou se são somente apresentadas oscilações pontuais.

## O que os dados revelam?

Os dados analisados permitem observar que a criminalidade nas regiões estudadas
apresentou redução entre 2023 e 2025.

Considerando os principais indicadores, crimes patrimoniais apresentaram a maior
redução, enquanto lesões corporais apresentaram o maior crescimento, segundo o KPI de
variação percentual.

A análise mensal demonstra ainda não indicou a existência de padrões de
concentração de ocorrências em determinados períodos do ano. Da mesma forma, os
dados indicam melhora nos indicadores criminais analisados.

Entretanto, é importante observar que a redução ou aumento dos registros criminais
não permite, isoladamente, concluir que houve melhora ou piora na eficiência das políticas
de segurança pública. Outros fatores devem ser incluídos na interpretação para realizar
esta afirmação.

## Quais indicadores representam melhor o problema?

Para representar a evolução da criminalidade, os indicadores de variação percentual
e tendência mensal são preferíveis, uma vez que aquele permite identificar a magnitude da
mudança, enquanto este permite avaliar se essa mudança é consistente ou resultado de
oscilações pontuais.

## Como os indicadores apoiam a tomada dedecisão?

Os indicadores permitem identificar quais tipos de crime apresentam o maior
crescimento e em quais períodos ocorre a maior concentração de determinadas
ocorrências.

Essas informações podem auxiliar gestores públicos na definição de prioridades,
direcionamento de recursos, planejamento de ações preventivas e acompanhamento de
resultados.

Além disso, com o acompanhamento periódico dos KPIs permite comparar a
evolução dos indicadores ao longo do tempo e verificar se determinadas medidas estão
associadas a mudanças nos registros criminais.

## Obtenção dos dados

Os dados utilizados neste trabalho são provenientes da Secretaria da Segurança
Pública do Estado de São Paulo (SSP-SP), responsável pela disponibilização do dataset
utilizado nessa análise.

O conjunto de dados contém registros mensais de diferentes naturezas criminais de
diferentes regiões, abrangendo o período de Janeiro de 2001 a Dezembro de 2026. O
dataset analisado contém informações apenas do período de Janeiro de 2023 a Dezembro
de 2025.

### Fonte

Dataset disponível em: <https://www.ssp.sp.gov.br/estatistica/dados-mensais>. Acesso em
23 ago. 2026.
