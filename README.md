# ⚛️ Simulação de Sistemas Quânticos com Python

Este projeto é um notebook desenvolvido durante a Escola de Matéria Quântica Avançada na UFAM. O objetivo é demonstrar a aplicação de métodos computacionais para simular e visualizar o comportamento de sistemas quânticos, utilizando a biblioteca NumPy para operações de Álgebra Linear.

## 📖 Contexto Teórico
A simulação se baseia na resolução numérica de uma equação de campo médio para um modelo da Física Estatística, similar ao Modelo de Ising. O notebook explora como o parâmetro de ordem (magnetização `m`) varia com a temperatura (`t`), revelando uma transição de fase em uma temperatura crítica.

## 💻 Metodologia Computacional
Para encontrar o valor de `m` que satisfaz a equação auto-consistente para cada temperatura, foi implementado o **método de Newton-Raphson**. O algoritmo iterativamente refina uma estimativa para a raiz da função, utilizando sua derivada (calculada numericamente) para convergir rapidamente para a solução.

## 🚀 Tecnologias e Conceitos
- **Python**
- **NumPy:** Para toda a manipulação de matrizes e vetores.
- **Matplotlib:** Para a visualização dos resultados.
- **Física Estatística & Cálculo Numérico**

## 📂 Como Utilizar
O projeto está em formato de notebook (`.ipynb`) e pode ser visualizado diretamente no GitHub ou executado interativamente no Google Colab.
