# Unifor
``` mermaid 
flowchart TD
A([INICIO])  --> B{{Digite um número:}}
B --> C[/número/]
C --> D{número > 0}
D --NÃO--> E{{O número deve ser positivo!}}
E --> J
D--SIM-->F[Resto é igual a número % 2]
F --> G{resto == 0}
G --NÃO--> H{{O número é ímpar!}}
G --SIM--> I{{O número é par!}}
H-->J([FIM])
I-->J


``` 
```
ALGORITMO verifica_par_impar
DECLARE número, resto INTEIRO
ESCREVA "Digite um número:"
LEIA número
SE número > 0 ENTÃO
    resto = número % 2
    SE resto == 0 ENTÃO
     ESCREVA "O número é par!"
  SENÃO
    ESCREVA "O número é ímpar!"
SENÃO
    ESCREVA "O número deve ser positivo!"
FIM_ALGORITMO
```
