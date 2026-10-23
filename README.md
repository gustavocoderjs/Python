# Python Básico 🐍

Repositório de estudos para **aprender Python do zero ao intermediário**, com exemplos práticos em arquivos `.py`.

O estudo começa pelos fundamentos da linguagem (tipos, variáveis, entrada e saída) e avança pelos operadores e estruturas de controle de fluxo. Depois vêm as **estruturas de dados** (listas, sets) e as **funções**. A trilha termina na **orientação a objetos** (herança, polimorfismo) e nos **frameworks web** (FastAPI, Flask), com um projeto prático de sistema bancário.

---

## 📚 Sumário

- [Proposta do projeto](#-proposta-do-projeto)
- [Trilha de estudos](#-trilha-de-estudos)
  - [Nível 1 — Fundamentos](#nível-1--fundamentos)
  - [Nível 2 — Operadores e controle de fluxo](#nível-2--operadores-e-controle-de-fluxo)
  - [Nível 3 — Estruturas de dados](#nível-3--estruturas-de-dados)
  - [Nível 4 — Funções e orientação a objetos](#nível-4--funções-e-orientação-a-objetos)
  - [Nível 5 — Bibliotecas e frameworks](#nível-5--bibliotecas-e-frameworks)
  - [Projeto prático](#-projeto-prático)
- [Estrutura do repositório](#-estrutura-do-repositório)
- [Como executar](#-como-executar)
- [Glossário rápido](#-glossário-rápido)
- [Referências](#-referências)

---

## 🎯 Proposta do projeto

Este repositório é um **caderno de aprendizado** de Python. Cada arquivo trata de um conceito, com exemplos curtos e comentados, para ser fácil de consultar depois.

### O que significa "do básico ao intermediário"?

O conteúdo segue uma ordem em que cada etapa usa o que foi aprendido na anterior:

1. **Fundamentos: escrever e ler dados.** Conhecer os tipos primitivos do Python (`int`, `float`, `bool`, `str`), declarar variáveis e constantes, converter tipos e interagir com o usuário via `input()`/`print()`.
2. **Operadores e controle de fluxo: tomar decisões e repetir ações.** Usar operadores de comparação, lógicos, identidade e associação para criar condições; usar `if`/`elif`/`else` e os laços `while`/`for` para controlar o fluxo do programa.
3. **Estruturas de dados: organizar informações.** Trabalhar com **listas** (indexação, fatiamento, list comprehension) e **sets** (conjuntos sem duplicatas, operações matemáticas de união e diferença).
4. **Funções e OOP: reutilizar e modelar.** Criar funções com parâmetros e retorno múltiplo; modelar entidades do mundo real com classes, herança (`super()`) e polimorfismo.
5. **Bibliotecas e frameworks: ir além do Python puro.** Usar **NumPy** para operações vetorizadas, construir APIs REST com **FastAPI** e **Flask**, consumir APIs externas com `requests` e orquestrar tarefas com **Apache Airflow**.

---

## 🧭 Trilha de estudos

### Nível 1 — Fundamentos

| Conceito | Descrição | Arquivo |
|----------|-----------|---------|
| Introdução | Primeiro programa, tipos primitivos (`int`, `float`, `bool`, `str`) e `print` | [introducao.py](introducao.py) |
| Variáveis e constantes | Declaração de variáveis, convenção `UPPER_CASE` para constantes e atribuição múltipla | [variaveis_constantes.py](variaveis_constantes.py) |
| Conversão de tipos | Converter entre `int`, `float` e `str`; divisão inteira com `//` | [convertendo_tipos.py](convertendo_tipos.py) |
| Entrada e saída | Receber dados do usuário com `input()` e exibir com `print()` | [entrada_saida.py](entrada_saida.py) |
| Strings | Métodos (`upper`, `lower`, `strip`, `center`, `join`), f-strings e fatiamento | [classe_string.py](classe_string.py) |

```python
nome = "Gustavo"
idade = 28

print(f"Olá, me chamo {nome} e tenho {idade} anos.")  # f-string
print(nome[::-1])   # fatiamento: inverte a string
print(nome.upper()) # GUSTAVO
```

### Nível 2 — Operadores e controle de fluxo

| Conceito | Descrição | Arquivo |
|----------|-----------|---------|
| Operadores de atribuição | `+=`, `-=`, `*=`, `/=`, `//=`, `%=`, `**=` | [operadores_atribuicao.py](operadores_atribuicao.py) |
| Operadores de comparação | `==`, `!=`, `>`, `<`, `>=`, `<=` | [operadores_comparacao.py](operadores_comparacao.py) |
| Operadores lógicos | `and`, `or`, `not` e combinações em expressões condicionais | [operadores_logicos.py](operadores_logicos.py) |
| Operadores de identidade | `is`, `is not` — verificam se dois objetos são o mesmo na memória | [operadores_identidade.py](operadores_identidade.py) |
| Operadores de associação | `in`, `not in` — verificam presença em sequências e conjuntos | [operadores_associacao.py](operadores_associacao.py) |
| Estrutura condicional | `if`/`elif`/`else` e operador ternário (`x if cond else y`) | [estrutura_condicional.py](estrutura_condicional.py) |
| Estruturas de repetição | `while`, `for`, `range()`, loops aninhados e iteração com `enumerate` | [estruturas_repeticao.py](estruturas_repeticao.py) |

```python
saldo = 1000
saque = 250
conta_especial = True

pode_sacar = (saldo >= saque) or conta_especial
print(pode_sacar)  # True

numero = 7
paridade = "Par" if numero % 2 == 0 else "Ímpar"
print(paridade)    # Ímpar
```

### Nível 3 — Estruturas de dados

| Conceito | Descrição | Arquivo |
|----------|-----------|---------|
| Listas | Indexação, fatiamento, `append`, listas aninhadas e série de Fibonacci | [lists.py](lists.py) |
| List comprehension | Sintaxe compacta `[expr for item in iterável]` para criar listas | [list_comprehesion.py](list_comprehesion.py) |
| List comprehension (avançado) | Mais exemplos e combinações com condições | [list_comprehesion2.py](list_comprehesion2.py) |
| Sets (conjuntos) | Unicidade automática, iteração com `for`/`enumerate`, `union`, `difference`, `issubset` | [set.py](set.py) |

```python
# List comprehension
quadrados = [i**2 for i in range(1, 11)]
print(quadrados)  # [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Sets não guardam duplicatas
linguagens = {"python", "java", "python"}
print(linguagens)  # {'python', 'java'}
```

### Nível 4 — Funções e orientação a objetos

| Conceito | Descrição | Arquivo |
|----------|-----------|---------|
| Funções | Definição com `def`, parâmetros posicionais e retorno múltiplo com tupla | [funcoes.py](funcoes.py) |
| Herança | Classe base e classe derivada; reutilização de `__init__` com `super()` | [heranca.py](heranca.py) |
| Polimorfismo | Mesmo nome de método com comportamentos diferentes em classes distintas | [polimorfismo.py](polimorfismo.py) |

```python
# Retorno múltiplo
def retorna_antecessor_e_sucessor(n):
    return n - 1, n + 1

ant, suc = retorna_antecessor_e_sucessor(10)
print(ant, suc)  # 9 11

# Polimorfismo
class Cachorro:
    def andar(self): print("quatro patas")

class Robo:
    def andar(self): print("rodas")

for obj in [Cachorro(), Robo()]:
    obj.andar()
```

### Nível 5 — Bibliotecas e frameworks

| Conceito | Descrição | Arquivo |
|----------|-----------|---------|
| NumPy | Performance: operação vetorizada com array vs. list comprehension em 1 M de elementos | [np.py](np.py) |
| FastAPI | API REST com `@app.get`, tipagem de parâmetros e retorno JSON | [fast_api.py](fast_api.py) |
| Flask (herança de views) | Classe base `MethodView` com log e resposta padronizada, herdada por outras views | [flask-heranca.py](flask-heranca.py) |
| Consumo de API externa | `requests.get` com parâmetros, tratamento de status code e exibição com `pprint` | [api-hashtag.py](api-hashtag.py) |
| Apache Airflow | Criação de DAG com `EmptyOperator` e `BashOperator`, dependências em série e paralelo | [first_dag.py](first_dag.py) |

**FastAPI, exemplo:**

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/vendas/{id_venda}")
def pegar_venda(id_venda: int):
    return vendas.get(id_venda, {"Erro": "ID não existe"})
```

**NumPy vetorização, exemplo:**

```python
import numpy as np

array = np.array(range(1_000_000))
quadrados = array ** 2  # muito mais rápido que list comprehension
```

### 🏦 Projeto prático

| Projeto | Descrição | Arquivo |
|---------|-----------|---------|
| Sistema Bancário | CLI interativo com depósito, saque (limite R$ 500 / 3 saques/dia), extrato e validações | [sistema_bancario.py](sistema_bancario.py) |

```sh
python sistema_bancario.py
```

### 🚧 Próximos tópicos (roadmap)

- [ ] Dicionários (`dict`) e tuplas
- [ ] Tratamento de exceções (`try`/`except`/`finally`)
- [ ] Módulos e pacotes (organização de projetos)
- [ ] Decorators e geradores
- [ ] Testes unitários com `pytest`
- [ ] Programação assíncrona (`async`/`await`)

---

## 📁 Estrutura do repositório

```
Python-basico/
├── README.md
├── introducao.py               # Tipos primitivos e print
├── variaveis_constantes.py     # Variáveis, constantes e atribuição múltipla
├── convertendo_tipos.py        # Conversão entre tipos
├── entrada_saida.py            # input() e print()
├── classe_string.py            # Métodos de string, f-strings e slicing
├── operadores_atribuicao.py    # +=, -=, *=, /=, etc.
├── operadores_comparacao.py    # ==, !=, >, <, >=, <=
├── operadores_logicos.py       # and, or, not
├── operadores_identidade.py    # is, is not
├── operadores_associacao.py    # in, not in
├── estrutura_condicional.py    # if/elif/else e operador ternário
├── estruturas_repeticao.py     # while, for, range() e loops aninhados
├── lists.py                    # Listas: indexação, fatiamento e Fibonacci
├── list_comprehesion.py        # List comprehension básico
├── list_comprehesion2.py       # List comprehension avançado
├── set.py                      # Conjuntos e operações matemáticas
├── funcoes.py                  # Funções e retorno múltiplo
├── heranca.py                  # Herança e super()
├── polimorfismo.py             # Polimorfismo
├── np.py                       # NumPy: lista vs. array
├── fast_api.py                 # API REST com FastAPI
├── flask-heranca.py            # Flask MethodView com herança
├── api-hashtag.py              # Consumo de API externa com requests
├── first_dag.py                # DAG no Apache Airflow
└── sistema_bancario.py         # Projeto: sistema bancário CLI
```

---

## ▶️ Como executar

### Pré-requisitos

- [Python 3](https://www.python.org/)
- Instalar as dependências do arquivo que deseja rodar (veja abaixo)

### 1. Clonar o repositório

```sh
git clone https://github.com/gustavocoderjs/Python-basico.git
cd Python-basico
```

### 2. Executar um arquivo simples (sem dependências externas)

```sh
python introducao.py
python sistema_bancario.py
```

### 3. Instalar dependências e executar a API FastAPI

```sh
pip install fastapi uvicorn
uvicorn fast_api:app --reload
```

Acesse [http://127.0.0.1:8000](http://127.0.0.1:8000) no navegador ou [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) para a documentação interativa.

### 4. Instalar dependências e executar o consumo de API externa

```sh
pip install requests
python api-hashtag.py
```

> ⚠️ O arquivo `api-hashtag.py` usa uma chave de API da [WeatherAPI](https://www.weatherapi.com/). Substitua o valor de `api_key` pela sua própria chave antes de rodar.

---

## 📖 Glossário rápido

| Termo | Significado |
|-------|-------------|
| **Tipo primitivo** | Tipo de dado básico: `int` (inteiro), `float` (decimal), `bool` (verdadeiro/falso), `str` (texto) |
| **Variável** | Nome que referencia um valor na memória |
| **Constante** | Variável cujo valor não deve mudar; convencionalmente em `UPPER_CASE` |
| **f-string** | String formatada com `f"..."` que permite interpolar variáveis diretamente no texto |
| **Slicing** | Fatiamento de sequências com a notação `[inicio:fim:passo]` |
| **List comprehension** | Forma compacta de criar listas: `[expr for item in iterável if cond]` |
| **Set** | Coleção sem duplicatas e sem ordem garantida |
| **Herança** | Mecanismo de OOP em que uma classe filha reutiliza atributos e métodos da classe pai |
| **Polimorfismo** | Capacidade de objetos de classes diferentes responderem ao mesmo método de formas distintas |
| **API REST** | Interface que expõe recursos via HTTP (GET, POST, PUT, DELETE) retornando JSON |
| **DAG** | *Directed Acyclic Graph*: grafo de tarefas sem ciclos, usado pelo Airflow para orquestrar pipelines |
| **Vetorização** | Operação aplicada a todos os elementos de um array de uma só vez, sem loop explícito (NumPy) |

---

## 🔗 Referências

- [Documentação oficial Python](https://docs.python.org/3/)
- [Documentação FastAPI](https://fastapi.tiangolo.com/)
- [Documentação Flask](https://flask.palletsprojects.com/)
- [Documentação NumPy](https://numpy.org/doc/)
- [Documentação Requests](https://requests.readthedocs.io/)
- [Documentação Apache Airflow](https://airflow.apache.org/docs/)

---

📌 *Repositório em constante evolução, acompanhando o avanço nos estudos de Python.*
