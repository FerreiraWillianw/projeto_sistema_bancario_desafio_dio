# 🏦 Sistema Bancário em Console com Python

## 📝 Descrição do Projeto

O projeto consiste em um sistema bancário simples desenvolvido em Python, operado via terminal (console). O principal objetivo é demonstrar a aplicação de conceitos de programação **procedural** e modularidade, organizando a lógica do sistema em funções bem definidas para cada operação.

O sistema gerencia dados de usuários e contas de forma simplificada, utilizando listas e dicionários para armazenamento em memória (os dados são voláteis e perdidos ao encerrar o programa).

### Funcionalidades Implementadas

O sistema oferece as seguintes opções no menu:

| Opção | Funcionalidade | Regras de Negócio Chave |
| :---: | :--- | :--- |
| `[d]` | **Depósito** | Aceita apenas valores positivos. |
| `[s]` | **Saque** | Validação de saldo, limite de R\$ 500 por saque e limite de 3 saques diários. |
| `[e]` | **Extrato** | Exibe todas as transações (depósitos e saques) e o saldo atual. |
| `[nu]` | **Novo Usuário** | Cadastra um cliente por CPF. Impede o cadastro de CPFs duplicados. |
| `[nc]` | **Nova Conta** | Cria uma conta corrente (`Agência: 0001`), vinculada a um usuário existente (identificado por CPF). |
| `[lc]` | **Listar Contas** | Exibe detalhes da agência, conta e titular para todas as contas. |
| `[q]` | **Sair** | Encerra o programa. |

### Destaques da Implementação em Python

Este código explora o uso de parâmetros de função para criar interfaces mais robustas e legíveis:

* **Modularização:** O código é bem dividido em funções (e.g., `depositar()`, `sacar()`) para facilitar a manutenção e o entendimento.
* **Argumentos Posicionais-Only (`/`):** A função `depositar(saldo, valor, extrato, /)` exige que os argumentos sejam passados **apenas pela posição**, garantindo uma chamada direta e concisa.
* **Argumentos Nomeados-Only (`*`):** A função `sacar(*, saldo, valor, ...)` exige que os argumentos subsequentes sejam passados **por palavra-chave** (`saldo=x`, `valor=y`), melhorando a clareza e prevenindo erros de ordem em funções com muitos parâmetros.

### Como Rodar o Projeto

1.  Clone este repositório para sua máquina local.
2.  Certifique-se de ter o Python 3 instalado.
3.  Execute o arquivo principal no seu terminal:

    ```bash
    sistema_bancario_simples.py
    ```
4.  Interaja com o menu no console.

---
