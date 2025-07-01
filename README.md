# SISTEMA PARA LOJA DE CONSTRUCAO 
---
# Sistema Loja de Material de Construção

Este sistema foi desenvolvido em Python com interface gráfica utilizando Tkinter e banco de dados SQLite. Ele permite o gerenciamento de produtos, clientes, vendas e despesas de uma loja de material de construção.

## Funcionalidades

- **Cadastro de Produtos:** Adicione novos produtos com nome e preço.
- **Listagem de Produtos:** Visualize todos os produtos cadastrados.
- **Cadastro de Clientes:** Registre clientes pelo nome.
- **Listagem de Clientes:** Visualize todos os clientes cadastrados.
- **Registro de Vendas:** Realize vendas à vista ou a prazo, vinculando produtos e clientes.
- **Registro de Despesas:** Lance despesas com descrição e valor.
- **Listagem de Vendas:** Veja todas as vendas realizadas, com detalhes de produto, cliente, data, quantidade, valor e status (pago/a prazo).
- **Relatórios de Renda:** Gere relatórios mensais ou anuais de ganhos, gastos e saldo.

## Estrutura do Banco de Dados

O sistema utiliza um banco SQLite chamado `loja_construcao.db` com as seguintes tabelas:

- **Produtos:** `id`, `nome`, `preco`
- **Clientes:** `id`, `nome`
- **Vendas:** `id`, `produto_id`, `cliente_id`, `data`, `quantidade`, `preco_unitario`, `total`, `pago`
- **Despesas:** `id`, `descricao`, `valor`, `data`

## Como Usar

1. **Executando o Sistema:**
   - Execute o arquivo principal loja_construcao_gui.py.
   - O banco de dados será criado automaticamente na primeira execução.

2. **Navegação:**
   - Utilize os botões do menu principal para acessar cada funcionalidade.
   - Para vendas a prazo, é necessário selecionar um cliente.

3. **Relatórios:**
   - Os relatórios exibem ganhos à vista, ganhos a prazo, total ganho, total gasto e saldo do período selecionado.

## Estrutura do Código

- Funções de conexão e criação do banco: `connect_db()`, `setup_db()`
- Classe principal da interface: `LojaApp`
  - Métodos para cada funcionalidade (cadastro, listagem, vendas, despesas, relatórios)

## Dependências

- Python 3.x
- Tkinter (incluso na maioria das instalações Python)
- SQLite3 (incluso na biblioteca padrão do Python)

