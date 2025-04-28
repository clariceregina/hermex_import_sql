# Gestão Banco de Dados Hermex Import

## 📋 Descrição

Este projeto tem como objetivo a criação e manipulação de um banco de dados do sistema comercial da Hermex Import, empresa de importação, incluindo tabelas de **fornecedores**, **pedidos**, **clientes**, **categorias** e **produtos**.

Foram realizadas operações de **criação de tabelas**, **inserção de dados**, **alteração de tabelas** e **consultas** básicas em SQL.

As consultas foram realizadas no SQLite Online.

---

## 🗂️ Estrutura do Banco de Dados

O projeto contém as seguintes tabelas:

- `tabela_fornecedores`: Armazena dados sobre fornecedores, como nome, país de origem e informações de contato.
- `tabela_clientes`: Contém informações dos clientes, incluindo nome, contato e endereço.
- `tabela_pedidos`: Guarda informações de pedidos realizados, status, total do pedido, cliente relacionado e data estimada de envio.
- `tabela_categorias`: Define categorias de produtos.
- `tabela_produtos`: Registra os produtos disponíveis, ligados a uma categoria e a um fornecedor.

---

## 🧩 Relacionamentos

- Cada produto (`tabela_produtos`) está relacionado a:
    - Uma categoria (`tabela_categorias`) através do campo `categoria`.
    - Um fornecedor (`tabela_fornecedores`) através do campo `fornecedor`.
- Cada pedido (`tabela_pedidos`) está associado a um cliente (`tabela_clientes`) através do campo `cliente`.

---

## 📄 Principais Operações Executadas

- **Criação de Tabelas:** `CREATE TABLE`
- **Inserção de Dados:** `INSERT INTO`
- **Alteração de Tabelas:** `ALTER TABLE` (ex: adicionando novas colunas)
- **Exclusão de Tabelas:** `DROP TABLE`
- **Consultas SQL:** `SELECT`, `SELECT DISTINCT`, `WHERE`

---

## 📊 Exemplos de Consultas

- Selecionar todos os fornecedores da China:

    ```sql
    SELECT * FROM tabela_fornecedores WHERE pais_de_origem = 'China';
    ```

- Selecionar todos os clientes únicos da tabela de pedidos:

    ```sql
    SELECT DISTINCT cliente FROM tabela_pedidos;
    ```
