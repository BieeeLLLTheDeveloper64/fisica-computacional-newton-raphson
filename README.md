# ⚛️ Resolução Numérica de Equação de Campo Médio via Newton-Raphson

Este projeto implementa um código em Python para resolver uma equação auto-consistente complexa, derivada de um modelo de Física Estatística, utilizando o método numérico de Newton-Raphson. O objetivo é encontrar o comportamento de um parâmetro de ordem (magnetização `m`) em função da temperatura (`t`), revelando a existência de uma transição de fase, que logo em seguida é gerada um gráfico.

Este trabalho foi desenvolvido como parte da atividade da **Escola de Matéria Quântica Avançada na UFAM**.

## 📖 Contexto Físico/Matemático

O código modela um sistema, cuja magnetização `m` em uma dada temperatura `t` e com acoplamentos `Jx` e `Jy` é determinada pela raiz da equação `f1(Jx, Jy, t, m) = 0`.

A função `f1` é derivada de uma abordagem de Grupo de Renormalização em Campo Médio (RGMF), que é uma técnica poderosa para estudar o comportamento crítico e as transições de fase em sistemas de muitos corpos. O gráfico gerado de `m` vs `t` demonstra visualmente como o sistema transita de uma fase ordenada (magnetizada, `m > 0`) para uma fase desordenada (não-magnetizada, `m = 0`) à medida que a temperatura aumenta, com a temperatura crítica localizada onde a magnetização vai a zero.

## 💻 Metodologia Computacional

Para encontrar o valor de `m` que satisfaz a equação `f1(..., m) = 0` para cada valor de temperatura `t`, foi implementado o **método de Newton-Raphson**.

O algoritmo iterativamente refina uma estimativa para `m` usando a relação:
`m_novo = m_antigo - f1(m_antigo) / f1'(m_antigo)`

Onde a derivada `f1'(m_antigo)` é calculada numericamente através de uma aproximação de diferenças finitas. O processo para a cada temperatura quando a função `f1` se aproxima de zero com uma precisão pré-definida (`epson`).

## 🚀 Tecnologias e Conceitos

- **Python**: Linguagem principal para a implementação.
- **NumPy**: Utilizada para operações com arrays e para as funções estatísticas e de álgebra linear no cálculo das matrizes B.
- **Matplotlib**: Utilizada para a visualização dos dados e a geração do gráfico final.
- **Física Estatística**: Base teórica para o modelo.
- **Cálculo Numérico**: Aplicação do método de Newton-Raphson.

## 📂 Como Executar

1.  Garanta que você tenha `numpy` e `matplotlib` instalados:
    `pip install numpy matplotlib`
2.  Clone o repositório e navegue até a pasta.
3.  Execute o script:
    `Física Computacional.ipynb`

O script irá executar os cálculos, salvar os dados no arquivo `jy1.dat` e, ao final, exibir e salvar o gráfico `m_vs_t.png`.
