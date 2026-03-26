# Calculadora de Integração Numérica – Método do Trapézio (Python)

## Descrição do Projeto

Este projeto implementa uma calculadora de **integração numérica** utilizando o **Método do Trapézio**, com interface gráfica desenvolvida em Python utilizando a biblioteca Tkinter.

O sistema permite que o usuário insira uma função matemática (em termos de `x`), um intervalo de integração e parâmetros de cálculo. A aplicação então calcula a aproximação da integral definida, exibindo também uma tabela de valores, erro estimado e intervalo de confiança.

O objetivo do projeto é aplicar conceitos de cálculo numérico, programação orientada a objetos e desenvolvimento de interfaces gráficas.

---

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Interface Gráfica:** Tkinter
* **Bibliotecas:**

  * `math` (funções matemáticas)
  * `re` (manipulação de strings)
  * `decimal` (controle de precisão numérica)

---

## Funcionalidades

* Inserção de função matemática personalizada
* Cálculo da integral definida pelo Método do Trapézio
* Definição do número de trapézios (precisão)
* Controle do número de casas decimais
* Exibição de:

  * Tabela de valores (x e f(x))
  * Área aproximada
  * Erro de arredondamento
  * Intervalo de confiança
  * Altura dos trapézios
* Interface gráfica interativa

---

## Funcionamento

### Entrada do Usuário

O usuário deve informar:

* Valor inicial (a)
* Valor final (b)
* Número de trapézios (t)
* Número de casas decimais (c)
* Função matemática (em termos de x)

### Processamento

1. A função digitada é tratada e convertida para sintaxe Python
2. São gerados os pontos do intervalo
3. Aplica-se o Método do Trapézio:

   * Divide o intervalo em subintervalos
   * Calcula a soma das áreas dos trapézios
4. Calcula-se o erro de arredondamento
5. Gera-se um intervalo de confiança para o resultado

---

## Fórmula Utilizada

A área é aproximada por:

Área ≈ (h/2) * [f(x0) + f(x1) + f(x1) + f(x2) + ... + f(xn)]

Onde:

* h = (b - a) / n
* n = número de trapézios

---

## Exemplos de Uso

### Entrada:

a = 0
b = 2
t = 4
c = 2
f(x) = x^2

### Saída:

x     f(x)
0.00  0.00
0.50  0.25
1.00  1.00
1.50  2.25
2.00  4.00

Área Total: 2.75
Erro de arredondamento: 0.01
Intervalo: [2.74, 2.76]
Altura do trapezio: 0.50

---

## Interface Gráfica

A aplicação possui uma interface simples onde o usuário pode:

* Inserir os valores nos campos de entrada
* Clicar no botão "Calcular"
* Visualizar o resultado em uma nova janela

---

## Observações Importantes

* A função é interpretada dinamicamente usando `eval`, portanto deve ser inserida corretamente
* Alguns símbolos são convertidos automaticamente:

  * √ → sqrt
  * π → pi
  * sen → sin
* O uso de `Decimal` melhora a precisão no cálculo do erro
* O número de trapézios influencia diretamente a precisão do resultado
* Não há validação completa de entrada, podendo ocorrer erros com funções inválidas

---

## Conceitos Praticados

* Integração Numérica (Método do Trapézio)
* Programação Orientada a Objetos (POO)
* Interfaces Gráficas com Tkinter
* Manipulação de expressões matemáticas
* Precisão numérica
* Estruturação de aplicações em Python
