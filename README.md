## Apresentação do Repositório

Bem-vindo ao repositório de Matemática Aplicada usando Python! Este repositório foi desenvolvido para o curso de Análise e Desenvolvimento de Sistemas e contém uma série de códigos focados em Matemática Aplicada. Todos os códigos foram ajustados e desenvolvido afim de ajudar aqueles que desejam se aperfeiçoar na área e na resolução das atividades.


## Conteúdos Abordados

- [Conversores Hexadecimal, decimal e binário](#conversores-hexadecimal-decimal-e-binário)
- [Tabela ASCII](#tabela-ascii)
- [Notação Científica](#notação-científica)
- [Cálculo Z-Score Probabilidade](#cálculo-z-score-probabilidade)
- [Probabilidade Simples (Slovin)](#probabilidade-simples-slovin)
- [Produto Escalar de Vetores](#produto-escalar-de-vetores)
- [Cálculo Desvio Padrão](#cálculo-desvio-padrão)
- [Calculadora de Mediana](#calculadora-de-mediana)
- [Calculadora de Média](#calculadora-de-média)
- [Criptografia - Cifra de César](#criptografia---cifra-de-césar)
- [Interpolação de Lagrange](#interpolação-de-lagrange)
- [Conversor de Moeda](#conversor-de-moeda)
- [Conversão para Bytes e Binário](#conversão-para-bytes-e-binário)
- [Cálculo de Bhaskara](#cálculo-de-bhaskara)
- [Proposições Possíveis](#proposições-possíveis)

## Bibliotecas

As bibliotecas utilizadas nos códigos são carregadas no início de cada script.

## Exemplos de Códigos

### Conversores Hexadecimal, decimal e binário
```python
def decimal_para_hexadecimal(numero_decimal):
    return hex(numero_decimal)

def hexadecimal_para_decimal(numero_hexadecimal):
    return int(numero_hexadecimal, 16)

def binario_para_decimal(binario):
    decimal = 0
    potencia = 0
    for digito em reversed(binario):
        if digito == '1':
            decimal += 2 ** potencia
        potencia += 1
    return decimal

def menu_conversao():
    case = int(input("Digite 1 para converter para hexadecimal ou 2 para converter para decimal ou 3 para converter para binario: "))
    if case == 1:
        numero_decimal = int(input("Digite um número decimal: "))
        numero_hexadecimal = decimal_para_hexadecimal(numero_decimal)
        print("O número hexadecimal correspondente é:", numero_hexadecimal)
    elif case == 2:
        numero_hexadecimal = input("Digite um número hexadecimal: ")
        numero_decimal = hexadecimal_para_decimal(numero_hexadecimal)
        print("O número decimal correspondente é:", numero_decimal)
    elif case == 3:
        numero_binario = input("Digite um número binário: ")
        numero_decimal = binario_para_decimal(numero_binario)
        print("O número decimal correspondente é:", numero_decimal)

menu_conversao()
```

### Interpolação de Lagrange
```python
import numpy as np

vet1_input = input("Digite a lista de valores separados por espaço X: ")
vet2_input = input("Digite a lista de valores separados por espaço Y: ")

vet1 = [float(i) for i in vet1_input.split()]
vet2 = [float(j) for j em vet2_input.split()]

x = np.array(vet1)
y = np.array(vet2)

polinomio = np.polyfit(x, y, len(x) - 1)

print("Polinômio interpolador de Lagrange:")
print(np.poly1d(polinomio))
```

## Proposições Possíveis

### Negação (∼):
- ∼𝑉 = 𝐹
- ∼𝐹 = 𝑉

### Conjunção "E" "." (∧):
- 𝑉 ∧ 𝑉 = 𝑉
- 𝑉 ∧ 𝐹 = 𝐹
- 𝐹 ∧ 𝑉 = 𝐹
- 𝐹 ∧ 𝐹 = 𝐹

### Disjunção "OU" + (∨):
- 𝑉 ∨ 𝑉 = 𝑉
- 𝑉 ∨ 𝐹 = 𝑉
- 𝐹 ∨ 𝑉 = 𝑉
- 𝐹 ∨ 𝐹 = 𝐹

### Implicação (→):
- 𝑉 → 𝑉 = 𝑉
- 𝑉 → 𝐹 = 𝐹
- 𝐹 → 𝑉 = 𝑉
- 𝐹 → 𝐹 = 𝑉

### Bicondicional (↔):
- 𝑉 ↔ 𝑉 = 𝑉
- 𝑉 ↔ 𝐹 = 𝐹
- 𝐹 ↔ 𝑉 = 𝐹
- 𝐹 ↔ 𝐹 = 𝑉

## Contribuições

Sinta-se à vontade para contribuir com este projeto. Envie um pull request com suas melhorias e correções.
