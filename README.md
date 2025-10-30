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

# 🔄️ Atualização do projeto para v2 'sistema_bancario_complexo.py'

# 🏦 Sistema Bancário em Python (v2 - Orientação a Objetos Básica)

Este projeto é uma aplicação de linha de comando que simula operações bancárias básicas, desenvolvida como exercício de consolidação dos princípios da **Programação Orientada a Objetos (POO)** em Python.

A principal mudança desta versão é a migração do modelo puramente procedural (variáveis soltas) para o modelo de classes, organizando o código e centralizando a lógica de negócio.

## ✨ Conceitos de POO Aplicados

| Conceito | Aplicação no Código | Detalhe |
| :--- | :--- | :--- |
| **Classes e Objetos** | `Cliente` e `ContaCorrente` | O usuário e a conta agora são **objetos** que contêm seus próprios dados (atributos) e comportamentos (métodos). |
| **Atributos Públicos** | `self.saldo`, `self.cpf` | Simplificação inicial: os dados são acessados diretamente (sem `@property` ou `_`). |
| **Associação** | `self.cliente` na classe `ContaCorrente` | A conta guarda uma **referência** ao objeto `Cliente`, permitindo acessar o nome do titular (ex: `conta.cliente.nome`). |
| **Comportamento Centralizado** | Métodos `depositar()` e `sacar()` | Toda a lógica de verificação de limites e atualização do saldo está **dentro** da classe `ContaCorrente`. |

4.  Interaja com o menu no console.

---
