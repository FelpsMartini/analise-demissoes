![Imagem](https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%201%20Capa.jpg)

# **Análise da Rotatividade de Funcionários**

## Sumário
1. [Objetivos](#1-objetivos)
2. [Visão Geral](#2-visão-geral)
3. [Colunas Quantitativas](#3-colunas-quantitativas)
4. [Correlações](#4-correlações)
5. [Histogramas](#5-histogramas)
6. [Uma Pausa na Programação](#6-uma-pausa-na-programação)
7. [Colunas Qualitativas](#7-colunas-qualitativas)
8. [Gráficos](#8-gráficos)
9. [Conclusão](#9-conclusão)

---

### 1. Objetivos
**Entender possíveis motivos que levaram os funcionários a pedir demissão**  

Para isso:  
Analisamos as variáveis quantitativas do grupo que ainda está na empresa versus o grupo que pediu demissão;
Destacamos aquelas que mais se diferenciavam em média, mediana, desvio padrão e quartis na comparação;
Depois, com as variáveis qualitativas, criamos uma tabela de frequências absolutas agrupadas.
Por fim, fizemos análises que misturavam colunas numéricas com categóricas.

    

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 2. Visão Geral
**Big numbers: uma breve descrição (quantitativa) da base de dados**   
Ao rodar alguns códigos com Pandas, descobrimos o seguinte:
- Há 1470 observações;  
- São 35 colunas (variáveis) no total: 26 numéricas e 9 categóricas;  
- 237 funcionários da base pediram demissão, contra 1233 que ainda trabalham na empresa.

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 3. Colunas Quantitativas
**Variáveis quantitativas: quando tudo é importante, nada é importante**  
Após dar um `df.groupby('Demissão').describe().T` , escolhemos as colunas quantitativas que mais eram relevantes para seguir com as análises:  
- Idade   
- Renda Mensal  
- Nível Hierárquico  
- Total de Anos Trabalhados (e seus similares)  


[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 4. Correlações
**De -1 a 1: uma ajudinha extra da relação entre as variáveis**  
Utilizamos a matriz de correlação para, junto com as medidas de tendência central e dispersão, ir a fundo em variáveis que possam justificar os pedidos de demissão.

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%206%20Correla%C3%A7%C3%B5es.jpg" width="80%" height="40%" alt="Correlações">

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 5. Histogramas
**Em alguns casos, junto é melhor que separado**  
Para analisar as colunas númericas que consideramos mais relevantes, usamos histogramas para ter uma visualização melhor das diferenças entre o grupo que pediu demissão versus os funcionários atuais.

**Idade**  
Observamos maior concentração dos funcionários que pediram demissão está na faixa de 25 a 35 anos, com um pico em torno de 30 anos.
A faixa de idade para funcionários que ainda estão na empresa é mais ampla, com um pico próximo dos 35 anos, mas com uma distribuição mais suave e frequente entre 25 e 45 anos.  

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%208%20Idade.jpg" width="80%" height="40%" alt="Distribuição de Demissões por Idade">

**Renda Mensal**  
A maioria dos funcionários que pediram demissão tem uma renda mensal concentrada abaixo de R$ 5.000,00

Embora a maioria dos funcionários que continuam na empresa também esteja concentrada em faixas salariais mais baixas, a distribuição é um pouco mais dispersa e há uma quantidade notável de funcionários com renda acima de R$ 10.000,00 e até em torno de R$ 20.000,00

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%209%20Renda%20Mensal.jpg" width="80%" height="40%" alt="Correlações">

**Anos Trabalhados**  
A maioria dos funcionários que pediram demissão tem menos de 5 anos de empresa. Isso é evidenciado pela alta concentração de pedidos de demissão entre 0 e 5 anos de tempo de serviço

Para os funcionários que permanecem, a distribuição é mais equilibrada, mas ainda há uma concentração significativa nos primeiros anos de trabalho, especialmente entre 0 e 10 anos

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2010%20Anos%20Trabalhados.jpg" width="80%" height="40%" alt="Correlações">  

**Anos Trabalhados com o atual gestor**  
A maior parte dos funcionários que pediram demissão trabalhou com o atual gestor por menos de 2 anos
Para os funcionários que ainda estão na empresa, há muitos funcionários na faixa de 0 a 3 anos com o gestor atual
Além disso, há períodos mais longos (5 a 10 anos), sugerindo que uma relação sólida e duradoura com o gestor pode estar associada à retenção

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2011%20Anos%20Trabalhados%20com%20o%20atual%20gestor.jpg" width="80%" height="40%" alt="Correlações">


[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 6. Uma Pausa na Programação
**Nível Hierárquico: uma variável quanti ou quali? Eis a questão**  
A maior parte dos pedidos de demissão vem de funcionários no Nível Hierárquico 1, com uma quantidade de demissões muito superior aos demais níveis

Já nos funcionários que ainda estão na empresa, o destaque está no Nível 2, que possui a maior quantidade de funcionários retidos

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2012%20Uma%20pausa%20na%20programa%C3%A7%C3%A3o.jpg" width="80%" height="40%" alt="Correlações">

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 7. Colunas Qualitativas
**Variáveis Categóricas: frequências, contagens e proporções**  
Decidimos investigar todas as colunas qualitativas:  
- Viagem de Negócios  
- Departamento  
- Área de Formação  
- Cargo  
- Estado Civil  
- Faz Hora Extra  

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 8. Gráficos  
**Viagem de Negócios**  
A tabela abaixo do gráfico destaca que, mesmo com uma quantidade absoluta de funcionários que “viaja raramente” e “não viaja”, a taxa de demissão é mais alta no grupo que “viaja frequentemente”.

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2014%20Viagem%20de%20Neg%C3%B3cios.jpg" width="80%" height="40%" alt="Correlações">

**Departamento:**  
Proporcionalmente, os funcionários do Departamento de Vendas são mais propensos a pedir demissão em comparação com os outros departamentos.  
<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2015%20Departamento.jpg" width="80%" height="40%" alt="Correlações">

**Área de Formação**  
RH apresenta a maior razão de pedidos de demissão (0.350), o que indica que, funcionários com esta formação são mais propensos a um turnover.  
Com uma razão de demissão de 0.320, Ensino Técnico é a segunda área com a maior proporção de pedidos de demissão
<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2016%20%C3%81rea%20de%20Forma%C3%A7%C3%A3o.jpg" width="80%" height="40%" alt="Correlações">

**Cargo**  
Representante de Vendas apresenta a maior razão de demissão (0.660), indicando que funcionários neste cargo  têm uma chance significativamente maior de sair da empresa.
Esse alto índice pode estar relacionado a pressões de metas, ambiente de trabalho competitivo ou uma reestruturação no setor comercial da empresa.
<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2017%20Cargo.jpg" width="80%" height="40%" alt="Correlações">

**Estado Civil**  
A categoria "Solteiro" apresenta a maior razão de demissão (0.342857), indicando que, proporcionalmente, pessoas com este status têm uma chance significativamente maior de pedir demissão.

Isso pode sugerir que elas têm mais flexibilidade quanto a mudança de emprego, pois tem menos vínculos ou compromissos que tornariam a estabilidade no emprego uma prioridade.
<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2018%20Estado%20Civil.jpg" width="80%" height="40%" alt="Correlações">

**Faz Hora Extra**  
A proporção de demissão entre os funcionários que fazem hora extra é significativamente maior. Eles têm quase quatro vezes mais chance de pedir demissão

Isso sugere que a prática de fazer hora extra pode estar relacionada ao aumento de pedidos de demissão, possivelmente devido ao desgaste, ao aumento de carga de trabalho, por exemplo

<img src="https://github.com/FelpsMartini/analise-demissoes/blob/main/imagens/%23%2019%20Faz%20hora%20extra.jpg" width="80%" height="40%" alt="Correlações">

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

---

### 9. Conclusão
**E o que concluímos?**  
A análise revelou insights importantes sobre os fatores que levam os funcionários a pedirem demissão

Identificamos que departamentos de P&D (na figura do Técnico de Laboratório) e Vendas (Representante de Vendas), que fazem muitas horas extras ou viajam frequentemente, estão mais propensos a pedir demissão

[⬆️ Voltar ao topo](#análise-da-rotatividade-de-funcionários)

