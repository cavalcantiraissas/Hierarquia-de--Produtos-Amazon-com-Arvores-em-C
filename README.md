<h1 align="center">📈 Hierarquia de Produtos Amazon com Árvores em C</h1>
<p align="center"><i>Disciplina: Estrutura de Dados I — UFMT </i></p>

---

## 🧠 Sobre o Projeto

Este projeto foi desenvolvido como parte da disciplina **Estrutura de Dados I** no curso de **Ciência da Computação** da **Universidade Federal de Mato Grosso (UFMT)**.  
Seu objetivo é aplicar conceitos fundamentais de estruturas de dados em **um sistema real**, utilizando uma base massiva da Amazon para modelar:

- 🌳 **Árvore N-ária** (hierarquia de categorias)
- 🌲 **Árvore Binária de Busca (BST)** (produtos por preço)
- 🔄 Integração entre estruturas
- 🔐 **Thread Safety** com `pthreads`
- 📁 Processamento de arquivos CSV

---

## 🔗 Dataset Utilizado

📁 [Amazon Product Dataset 2023 - Kaggle](https://www.kaggle.com/datasets/asaniczka/amazon-products-dataset-2023-1-4m-products/data)

Arquivos principais:
- `amazon_products.csv` — mais de 1.4 milhão de produtos
- `amazon_categories.csv` — 270 categorias

---

## 🧱 Estrutura de Dados Utilizada

| Estrutura | Descrição |
|----------|-----------|
| **Árvore N-ária** | Representa a hierarquia de categorias e subcategorias (ex: Eletrônicos > Computador) |
| **BST (Árvore Binária de Busca)** | Armazena os produtos, usando o preço como chave |
| **Integração entre árvores** | Permite localizar produtos a partir de uma categoria e vice-versa |

---

## ⚙️ Funcionalidades

### 🏷️ Organização Hierárquica
- Classificação dos produtos em uma estrutura n-ária baseada nas áreas fornecidas (Casa, Eletrônicos, Pessoal, etc.)
- Alocação de categorias não mapeadas para a raiz “Diverso”

### 📦 Processamento de Produtos
- Leitura e validação de registros (remoção de preços inválidos)
- Inserção em árvore binária balanceada por preço
- Mapeamento dos produtos às respectivas categorias

### 📊 Consultas Disponíveis
Menu interativo via terminal com as seguintes opções:

1. Listar produtos com preços entre `X` e `Y`
2. Listar todos os produtos de uma categoria
3. Top 5 produtos mais caros por categoria
4. Top 5 produtos mais baratos por categoria

---

## 🖥️ Interface

- Terminal baseado em menus
- Geração automática de arquivos `.txt` com os resultados das consultas

---

## 🚀 Como Executar

### ✅ Pré-requisitos
- Sistema Unix (Linux/macOS)
- Compilador `gcc` com suporte a `-lpthread`

### 🧪 Passo a passo
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/amazon-arvores-c.git

# Acesse o diretório
cd amazon-arvores-c

# Compile o projeto
gcc -o amazon_produtos main.c categoria.c produto.c utils.c -lpthread -Wall

# Execute o programa (com os arquivos CSV no mesmo diretório)
./amazon_produtos
