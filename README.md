# Jogo da Velha - Análise de Dados

Este repositório contém um script Python para treinar um modelo de Machine Learning com base em um conjunto de dados do Jogo da Velha. O conjunto de dados inclui 958 amostras que representam todas as possíveis configurações do tabuleiro do Jogo da Velha.

## Descrição do Conjunto de Dados

O Jogo da Velha é um jogo para duas pessoas que requer apenas papel e lápis. O tabuleiro é uma matriz de três linhas por três colunas. Cada jogador se reveza desenhando uma cruz (x) ou um círculo (o) em uma posição desta matriz. O vencedor é aquele que conseguir colocar três peças iguais em uma fileira, na vertical, na horizontal ou na diagonal.

O conjunto de dados consiste em:

- Nove atributos (enumerados de 1 a 9) representando o estado de cada posição do tabuleiro (valores possíveis: x, o, b).
- Um rótulo de classe representando o desfecho da configuração (valores possíveis: "positivo" para vitória do x ou "negativo" para empate ou derrota do x).

O conjunto de dados foi traduzido de uma versão originalmente concebida por Aha [1] em 1991.

## Etapas para Execução

### 1. Baixar o Conjunto de Dados

Baixe o conjunto de dados em formato CSV (comma-separated-values) do [link](link_para_o_conjunto_de_dados).

### 2. Fazer a Leitura dos Dados

Utilize a biblioteca Pandas para fazer a leitura dos dados no script Python.

```python
import pandas as pd

data = pd.read_csv('caminho/para/seu/conjunto_de_dados.csv')
```
### 3. Converter Valores
Converta os valores presentes no conjunto de dados para números inteiros de acordo com o seguinte mapeamento:

o: -1
b: 0
x: 1
negativo: -1
positivo: 1

Utilize o método replace da classe DataFrame do Pandas.

```python
mapping = {'o': -1, 'b': 0, 'x': 1, 'negativo': -1, 'positivo': 1}
data.replace(mapping, inplace=True)
```

### 4. Executando o Modelo
Após seguir as etapas acima, o script Python treinará um modelo de classificação utilizando o conjunto de dados do Jogo da Velha.