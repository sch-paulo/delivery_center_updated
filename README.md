# Projeto de Engenharia de Dados - Delivery Center

<p align="center">
    <img src="pics\delivery_center.png"
</p>

Este projeto é um complemento de outro projeto: [análise de dados do Delivery Center](https://github.com/sch-paulo/delivery_center_data_analysis/), e consiste na conteinerização do projeto, empacotando todo o processo via Docker.

## Conjuntos de dados

Os dados utilizados estão distribuídos em sete tabelas, com informações sobre canais de venda, entregas, entregadores, hubs, pedidos, pagamentos e lojistas.

O modelo lógico do banco de dados é apresentado no seguinte formato:

<p align="center">
  <img src="pics/model.png" alt="Modelo relacional datasets">
</p>

## Apresentação
A análise é apresentada em duas frentes:

### Dashboard Interativo:
No dashboard encontram-se as principais métricas e indicadores que permitem uma compreensão da performance da empresa.

<p align="center">
  <img src="https://github.com/sch-paulo/delivery_center_data_analysis/assets/132720763/0e2a0050-ead8-4804-bd1d-378f271dbdc7" alt="Dashboard">
</p>

### [Confira aqui o dashboard do projeto.](https://app.powerbi.com/view?r=eyJrIjoiYWVhNGZiYjEtNTNlMC00MzNhLWEyOGQtMWY1ZDAxNDhkMGRlIiwidCI6IjE0ZDhhZDA3LWFmYWQtNGJmYS05M2QzLWEyMmIxYWFlNWU4NSJ9)

### Apresentação em PDF:
Esta apresentação oferece insights aprofundados sobre diversos aspectos da empresa, incluindo análises sobre cidades, hubs, entregas, entregadores, lojas, canais de venda e pagamentos. Além disso, ao final do documento, é elaborado um plano de ação contendo medidas visando o aprimoramento do desempenho geral da empresa.

## Ferramentas
Para a execução dessa análise, foram utilizadas algumas ferramentas, tais quais:
- **SQL**: As consultas foram estruturadas através do *DBeaver*, utilizando o SGBD *MySQL*.
- **Python**: Para realizar a conexão das tabelas .csv e o SGBD *MySQL*. <br /> O passo a passo está demonstrado no arquivo `conexao_sql.ipynb`.
- **Microsoft Power BI**: O dashboard do projeto foi construído com o uso do software, com a necessidade da criação de algumas funções em DAX para a construção das visualizações.
- **Microsoft PowerPoint**: Confecção da apresentação final com o panorama geral da empresa.

## Perguntas de Negócio

#### 1. Quais canais de venda geram mais receita para o Delivery Center? <br /> 
O canal *Food Place* representa mais de 70% da receita. Graças a ele, os *marketplaces* superaram *canais próprios* em mais de 4 vezes em receita.

#### 2. Qual a média de tempo de entrega por região? <br /> 
Curitiba, seguida por Porto Alegre, Rio de Janeiro e, por fim, São Paulo. Coincidentemente ou não, o tempo de entrega é inversamente proporcional ao volume de pedidos.

#### 3. Quantos entregadores únicos entregaram mais de 100 pedidos no período? <br /> 
Dos 4822 entregadores, cerca de 950 possuem mais de 100 entregas, o que dá aproximadamente 20% do total de entregadores.

#### 4. Qual o valor médio de pedido por tipo de pagamento? <br /> 
Variando de R$ 490,00 até R$14,00, o destaque fica para o pagamento *Online*, com valor médio de R$ 99,81 e representando 85% dos pagamentos.

#### 5. Top 15 lojas que mais geram receita entre fevereiro e março? <br /> 
Com mais de 6,6 milhões de reais em pedidos, *Iumpica* é líder isolada no ranking de receita do período. Completando o pódio, temos *Salito*, com 1,6 milhão e *Ipupiemai*, com 900 mil. <br />
Lojas do segmento alimentício (*food*) somaram 3,25 vezes mais receita do que o segmento de mercadorias (*good*).

#### 6. Qual o crescimento percentual mensal no número de pedidos por cidade/hub de distribuição? <br /> 
Se observa um padrão de queda de janeiro para fevereiro, logo após um grande salto de fevereiro para março e, por fim, uma estabilidade no volume de março para abril.

#### 7. Quem são os 5 entregadores com a maior média de entregas por dia, e como essa média varia mês a mês? <br /> 
A média variou de 9 a 14 entregas por dia, para os mais bem colocados em cada mês.

#### 8. Quais são os hubs com aumento de pedidos acima de 20% de fevereiro para março? <br /> 
Apenas quatro hubs não tiveram crescimento superior a 20% no período, e apenas um teve queda de pedidos.

#### 9. Qual a relação entre o número de entregas realizadas e o número de pedidos, por lojista? <br /> 
Um a cada oito lojistas apresentam um índice de entregas não realizadas acima de 5%.

#### 10. Qual o ranking dos top 10 lojistas com mais pedidos em cada canal de venda? <br /> 
Com apenas alguns chegando à marca dos 10 mil pedidos, *Iumpica* impressiona com seus mais de 94 mil pedidos somados.



## Instalação e Configuração

Siga estas etapas para utilizar esse projeto em sua máquina local:

1. Navegue até o diretório que deseja salvar os arquivos do projeto:
    ```bash
    cd meu_workspace
    ```

2. Clone o repositório:
   ```bash
   git clone https://github.com/sch-paulo/delivery_center_container.git
   ```

3. Navegue até o diretório do projeto:
   ```bash
   cd delivery_center_container
   ```

4. Certifique-se de possuir o Docker Desktop instalado em sua máquina:<br>
  **[Download do Docker Desktop](https://www.docker.com/products/docker-desktop/)**
<br>
5. Suba o docker-compose
    ```bash
    docker-compose up --build
    ```

7.
8
