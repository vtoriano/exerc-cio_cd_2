# Atividade 2 — Limpeza, Transformação e Agrupamento de Dados com Pandas

Notebook de exercícios práticos em Python utilizando a biblioteca **pandas** para análise do dataset de emendas parlamentares brasileiras.

## Dataset

**emendas_tratamento.parquet** — Dataset de emendas parlamentares com informações sobre valores empenhados, pagos, regiões, municípios, autores e funções orçamentárias.

- 📥 Download: [Google Drive](https://drive.google.com/file/d/19ydA23-eboyiKxN29JL1EQWW4CplTiKg/view?usp=sharing)

## Carregamento dos dados

```python
import pandas as pd

df = pd.read_parquet("https://drive.google.com/uc?export=download&id=19ydA23-eboyiKxN29JL1EQWW4CplTiKg")
```

## Exercícios

O notebook está organizado em 16 exercícios divididos em três categorias:

### 🔍 Filtragem de Dados (Exercícios 1–3)
| # | Descrição |
|---|-----------|
| 1 | Filtrar emendas do ano de **2022** e contar o total registrado |
| 2 | Filtrar emendas da região **Norte** com `Valor Empenhado` > R$ 500.000 |
| 3 | Filtrar emendas de **São Paulo** e **Rio de Janeiro** e comparar contagens |

### 🧹 Limpeza e Transformação (Exercícios 4–11)
| # | Descrição |
|---|-----------|
| 4 | Substituir valores `"Sem informação"` por `"Não disponível"` na coluna `Código da Emenda` |
| 5 | Converter `Nome Função` para letras maiúsculas |
| 6 | Identificar e remover **linhas duplicadas** do dataset completo |
| 7 | Remover duplicatas considerando apenas `Código da Emenda` e `Município` |
| 8 | Identificar colunas com **valores nulos** e suas contagens |
| 9 | Preencher nulos de `Código do Autor` com `-1` e `Nome do Autor` com `"desconhecido"` |
| 10 | Converter `Ano da Emenda` para o tipo **string** |
| 11 | Garantir que `Valor Empenhado` está no tipo **float** |

### 📊 Agrupamento e Análise (Exercícios 12–16)
| # | Descrição |
|---|-----------|
| 12 | Calcular **total de `Valor Pago`** por Região |
| 13 | Contar emendas por `Nome Função` e listar as 5 com mais ocorrências |
| 14 | Criar coluna `Saldo a Pagar` = `Valor Empenhado` − `Valor Pago` |
| 15 | Eliminar colunas **completamente vazias** do DataFrame |
| 16 | Exportar o DataFrame transformado para **JSON** |

## Requisitos

- Python 3.8+
- pandas
- pyarrow (para leitura de arquivos `.parquet`)

Instale as dependências com:

```bash
pip install pandas pyarrow
```

## Como usar

1. Clone ou baixe este repositório
2. Abra o arquivo `pandas_intro_ex2.ipynb` no Jupyter Notebook ou JupyterLab
3. Faça o download do dataset (link acima) e coloque-o na mesma pasta, **ou** use a URL direta no código
4. Execute as células em ordem, respondendo cada questão com código e interpretação em Markdown

## Estrutura do Notebook

Cada exercício segue o padrão:
- **Célula de código** — solução implementada em pandas
- **Célula de texto (Markdown)** — interpretação do resultado obtido
