# UNIFOR
**Nome**: Davi de Moura Pinheiro
**Disciplina**: Raciocínio Lógico Algorítmo

## Exercício 01 

Calcule a média de quatro números inteiros dados.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INÍCIO]) --> B{{"Digite o número 1:"}}
B --> C[/num1/]
C --> D{{"Digite o número 2:"}}
D --> E[/num2/]
E --> F{{"Digite o número 3:"}}
F --> G[/num3/]
G --> H{{"Digite o número 4:"}}
H --> I[/num4/]
I --> J["media = (num1 + num2 + num3 + num4)/4"]
J --> K{{A média é, media}}
K --> L([FIM])
```

## Pseudocódigo (1.0 ponto)

```java
ALGORTIMO Media
DECLARE num1, num2, num3, num4: REAL

INÍCIO

    // Solicita ao usuário que digite o número 1
    ESCREVA "Digite o número 1:"
    
    // Lê o número 1 fornecido pelo usuário
    LEIA num1

    // Solicita ao usuário que digite o número 2
    ESCREVA "Digite o número 2:"
    
    // Lê o número 2 fornecido pelo usuário
    LEIA num2

    // Solicita ao usuário que digite o número 3
    ESCREVA "Digite o número 3:"
    
    // Lê o número 3 fornecido pelo usuário
    LEIA num3

    // Solicita ao usuário que digite o número 4
    ESCREVA "Digite o número 4:"
    
    // Lê o número 4 fornecido pelo usuário
    LEIA num4

    // Calcula a média dos quatro números
    media <- (num1 + num2 + num3 + num4) / 4
    
    // Exibe a média
    ESCREVA "A média é", media

FIM


