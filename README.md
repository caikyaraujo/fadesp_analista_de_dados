### ✅ Etapa 1 – Desenvolvimento de Dashboard em Power BI

**Objetivo:** Verificar sua capacidade de análise de dados e construção de dashboards funcionais e informativos.

**Cenário:**  
Um cliente solicitou a criação de um painel com as seguintes análises:

- **Visão Geral das Vendas**
- **Análise Temporal**
- **Análise Geográfica**
- **Tabela de informações destrinchadas e agrupadas por Produto**

**Tarefas:**

- Usar os arquivos `.csv` disponíveis em `/etapa_1/data/`.
- Desenvolver o dashboard livremente no Power BI, utilizando os recursos necessários para atender ao escopo solicitado.
- Adicionar quaisquer tratamentos e visuais adicionais que considerar relevantes.
- Essa etapa valoriza principalmente a sua criatividade na escolha de visualizações e no uso dos recursos que o Power BI oferece.

**Painel:**

- **Análise de Vendas:** 
   **Cartões Superiores**
      - Mostra o total de vendas e volume de vendas de pedidos.
      - Valor dos pedidos "Em Processamento" e volume quantitativo desses pedidos.
      - Valor dos pedidos "Não Concluídos" e volume quantitativo desses pedidos.
   **Gráfico de Barras**
      - Análise de vendas por categoria.
      - Quantidade de produtos.
   **Gráfico de Linha**
      - Análise temporal das vendas e volume de pedidos.
   **Tabela Matriz**
      - Avaliações de produtos por categoria.
   **Mapa Geográfico**
      - Análise geógráfica de vendas baseada na região dos vendedores.

**Correções**
   - Tratamento de dados nas bases: categorias_produtos, vendedores, avaliacoes_pedidos, itens_pedidos, pedidos e produtos.
   - Correções no nome de cidades, estados e regiões, para que pudessem ser utilizados no mapa geográfico da forma correta.
   - Coluna "order_status" foi duplicada ("order_status_br") criando uma colunas com o nome do status em português.
      - aprooved para aprovado.
      - cancelled para cancelado.
      - created para criado.
      - delivered para entregue.
      - invoiced para faturado.
      - processing para em processamento.
      - shipped para enviado.
      - unavailable para indisponível.
   - Classificação dos status dos pedidos para que pudessem ser utilizados no dashboard de forma mais simples e direta, como:
      - "Em Processamento": criado e processamento 
      - "Não Concluídos": cancelado e indisponível
      - "Vendidos": aprovado, faturado, enviado e entregue.

**Considerações e Procedimentos**
   - Havia uma grande quantidade de inconsistência nos dados, como por exemplo, a falta de dados em algumas colunas, ou valores errados na escrita entre outros problemas.
   - Foi necessário realizar uma grande quantidade de tratamento de dados para que os dados pudessem ser o mais preciso possível.
   - A base de produtos havia uma grande quantidade de produtos não foram cadastrados corretamente, sem a descrição correta do produto, o valor aproximado de desse tipo de inconsistência é de 605 registros.
---

### ✅ Etapa 2 – Aplicação da Camada Semântica em Dados Quebrados

**Objetivo:** Avaliar sua capacidade de estruturar dados com qualidade, garantindo uma base sólida para análises consistentes e visuais eficazes.

**Cenário:**  
Um cliente forneceu um conjunto de dados sem qualquer tratamento prévio e solicitou a criação de uma visualização simples de tabela para análise.

**Tarefas:**

- Utilizar os arquivos `.csv` disponíveis em `/etapa_2/data/`.
- Estruturar o modelo de dados no Power BI, tratando possíveis inconsistências e preparando os dados para análises confiáveis.
- Criar apenas uma visualização em formato de tabela, acompanhada de filtros relevantes, conforme o escopo solicitado.
- Incluir quaisquer ajustes que considerar importantes para garantir clareza, integridade e utilidade das informações apresentadas.


**Painel:**

- **Arrecadações** 
   **Segmentações de dados**
      - Ano, Mês.
      - Estado.
      - Imposto.

   **Tabela**
      - Análise do valor acumulado de cada imposto por município.

**Correções**
   - Tratamento de dados na base: arrecadacao_impostos_municipais.
   - Correções no nomes dos impostos.
   - Exclusão de valores em branco

**Considerações e Procedimentos**
   - Havia uma grande quantidade de impostos que possuiam o último caracterer do seu nome duplicado, sendo assim gerando inconsistência nos dados.
   - Foi necessário realizar a exclusão de aproximadamente 200 valores que estavam em branco.
   - Foi uma análise simples e entregando a visualização solicitada em forma de tabela.
---

### ✅ Etapa 3 – Análise Exploratória com Python + SQL

**Objetivo:** Avaliar sua familiaridade com ferramentas de análise programática e manipulação de dados.

**Tarefas:**

1. **Extração:**
   - Utilize os dados presentes no diretório `/etapa_3/data/`.

2. **Armazenamento e Consulta:**
   - Salve os dados em um **banco SQLite**.
   - Realize consultas utilizando **SQL** diretamente nesse banco.

3. **Análise Exploratória:**
   - Utilize **pandas** e comandos SQL para explorar os dados.
   - Exiba **indicadores e visualizações** com bibliotecas gráficas como matplotlib, seaborn, plotly ou dash.
   - Comente e documente seu código adequadamente para facilitar o entendimento.
   - Fique livre para adicionar quaisquer features ou melhorias.

---

## 📌 Considerações Finais

- Este desafio não possui caráter eliminatório, mas **será um diferencial** no processo seletivo.
- Crie um **fork deste repositório no seu GitHub pessoal** e adicione nele:
  - Arquivos `.pbix` das Etapas 1 e 2
  - Arquivo `.ipynb` da Etapa 3 (notebook Python)

- Os arquivos disponibilizados no seu fork serão considerados os **entregáveis finais** do desafio.

---
