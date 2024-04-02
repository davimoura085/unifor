# UNIFOR
Nome: Davi de Moura Pinheiro
Disciplina: Raciocínio Lógico Algorítimico

## Lista de exercícios 03

### Exercício 01 (2.5 pontos)
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero. 

```mermaid
flowchart TD
title Verificar se um número é par ou ímpar

A([INICIO]) --> B{{Digite um número:}}
B --> C[\num\]
C --> D{num < 0}
D --FALSE--> E[resto = num % 2]
E --> H{resto == 0}
H --FALSE--> I{{O número é ímpar!}}
H --TRUE--> J{{O número é par!}}
I --> Z([FIM])
J --> Z
D --TRUE--> F{{Digite um número maior ou igual a zero:}}
F --> G[/num/]
G --LOOP--> D
Z --> Z([FIM])
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORITMO verifica_par_impar
DECLARE num, resto: INTEIRO

INÍCIO
	// Solicita ao usuário que insira um número inteiro
	ESCREVA "Digite um número inteiro: "

	// Armazena o valor de entrada na variável "num"
	LEIA num

	// Garante que o número seja não negativo
	ENQUANTO num < 0 FAÇA
		ESCREVA "Digite um número maior ou igual a zero: "
		LEIA num
	FIM_ENQUANTO

	// Verifica se o número é positivo
	SE num >= 0 ENTAO
		// Calcula o resto da divisão de "num" por 2
		resto ← num % 2
               
		// Verifica se o resto é igual a zero
		SE resto == 0 ENTAO
			ESCREVA "O número é par!"
		SENAO
			ESCREVA "O número é ímpar!"
		FIM_SE
	SENAO
		ESCREVA "O número deve ser positivo!"
	FIM_SE
FIM_ALGORITMO
```

#### Tabela de testes (0.5 ponto)

| num | num < 0 | num | resto | resto == 0 | saída             | 
| --  | --      | --  | --    | --         | --                | 
| -1  | True    | 0   | 0     | True       | O número é par!   |
| 1   | False   |     | 1     | False      | O número é impar! |
| 2   | False   |     | 0     | True       | O número é par!   |

### Exercício 02 (2.5 pontos)
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
title Iteração com Loop
desc Este fluxograma demonstra um loop que conta de 0 até n-1 com incremento de 3.

A([INICIO]) --> B{{Digite a quantidade de números:}}
B --> C[\n\]
C --> D[Inicialize i como 0]
D --> E[Enquanto i < n]
E --> F{{ESCREVA i}}
F --> G{{Incremente i por 3}}
G --> E
E --> H([FIM])
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORITMO MultiploTres
DECLARE n: INTEIRO

INÍCIO

	// Solicita ao usuário a quantidade de números desejada
	ESCREVA "Digite a quantidade de números:"

	// Armazena o valor de entrada na variável "n"
	LEIA n

	// Loop de contagem (para cada) executa as instruções para cada valor de 'i' de 0 até n-1, incrementando 'i' em 3.
	PARA i DE 0 ATÉ n-1 PASSO 3 FAÇA

		// Exibe o valor de 'i' em cada iteração
		ESCREVA i

	FIM_PARA

FIM_ALGORITMO
```

#### Tabela de testes (0.5 ponto)

| it | n   | i  | saida | 
| -- | --  | -- | --    |    
| 1  | 7   | 0  | 0     |
| 2  | 7   | 3  | 3     |
| 3  | 7   | 6  | 6     |

### Exercício 03 (2.5 pontos)
Dada uma sequência de números inteiros, calcular a sua soma. 
Por exemplo, para a sequência {12, 17, 4, -6, 8, 0}, o seu programa deve escrever o número 35.

#### Fluxograma 1

```mermaid
flowchart TD
title Soma de Números
desc Este fluxograma calcula a soma de n números inseridos pelo usuário.

A([INICIO]) --> B{{Digite a quantidade de números:}}
B --> C[\n\]
C --> D[i = 1]
D --> E[soma = 0]
E --> F{i <= n}
F --FALSE--> G{{A soma dos números é: soma}}
G --> L([FIM])
F --TRUE--> H{{Digite o número, i:}}
H --> I[\num\]
I --> J[soma = soma + num]
J --> K[i = i + 1]
K --LOOP--> F
```

#### Fluxograma 2

```mermaid
flowchart TD
title Soma de Números
desc Este fluxograma calcula a soma de n números inseridos pelo usuário.

A([INICIO]) --> B{{Digite a quantidade de números:}}
B --> C[\n\]
C --> D[soma = 0]
D --> E[[i=1 ATÉ n, PASSO 1]]
E --FALSE--> F{{A soma dos números é, soma}}
F --> L([FIM])
E --TRUE--> G{{Digite o número, i:}}
G --> H[\num\]
H --> I[soma = soma + num]
I --LOOP--> E
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORITMO SomaValores
DECLARE n, i: INTEIRO
DECLARE soma, num: REAL

INÍCIO

	// Solicita ao usuário a quantidade de números desejada
	ESCREVA "Digite a quantidade de números:"

	// Armazena o valor de entrada na variável "n"
	LEIA n

	// Inicializa a variável "soma" em 0
	soma <- 0

	// Inicializa a variável "i" em 1
	i <- 1

	// Loop condicional (enquanto) executa as instruções enquanto a condição "i <= n" for verdadeira
	ENQUANTO i <= n FAÇA

		// Solicita ao usuário que digite o número
		ESCREVA "Digite o número ", i, ":"

		// Armazena o valor de entrada na variável "num"
		LEIA num

		// Adiciona o valor de "num" à variável "soma"
		soma <- soma + num

		// Incrementa o contador "i" em 1
		i <- i + 1

	FIM_ENQUANTO

	// Exibe a soma dos números digitados
	ESCREVA "A soma dos números é ", soma

FIM_ALGORITMO
```

#### Tabela de testes (0.5 ponto)

| n  | soma | i  | i <= n | num | soma + num | i + 1   | saída                      |  
| -- | --   | -- | --     | --  | --         | --      | --                         |
| -1 | 0    | 1  | False  |     |            |         | A soma dos número é 0      |
| 0  | 0    | 1  | False  |     |            |         | A soma dos número é 0      |
| 3  | 0    | 1  | True   | 10  | 0+10 = 10  | 1+1 = 2 |                            |
| 3  | 10   | 2  | True   | 20  | 10+20 = 30 | 2+1 = 3 |                            |
| 3  | 30   | 3  | True   | 30  | 30+30 = 60 | 3+1 = 4 |                            |
| 3  | 60   | 4  | False  |     |            |         | A soma dos número é 60     |

### Exercício 04 (2.5 pontos)
Escreva um programa que leia a nota de diversos alunos, até que seja digitada uma nota negativa. 
Nesse momento, ele mostra a média aritmética de todas as notas lidas e quantas notas foram lidas. 
Ex. Foram lidas 14 notas. A média aritmética é 6.75!

#### Fluxograma

```mermaid
flowchart TD
title Cálculo da Média de Notas
desc Este fluxograma calcula a média aritmética das notas dos alunos.

A([INICIO]) --> B[/soma/]
B --> C[/cont/]
C --> D{{"Digite a nota do aluno (digite uma nota negativa para finalizar):"}}
D --> E{nota >= 0}
E --FALSE--> Z([FIM])
E --TRUE--> F{cont > 0}
F --FALSE--> G[media = soma / cont]
G --> H{{Foram lidas, cont, notas. A média aritmética é, media!}}
H --> Z
F --TRUE--> I[soma += nota]
I --> J[cont += 1]
J --> K{{"Digite a nota do aluno (digite uma nota negativa para finalizar):"}}
K --LOOP--> D
```

### Pseudocódigo

```java
ALGORITMO QuantMedia
DECLARE nota, soma, media: REAL
DECLARE cont: INTEIRO

INÍCIO
	
	// Solicita ao usuário a primeira nota do aluno (nota negativa finaliza)
	ESCREVA "Digite a nota do aluno (nota negativa finaliza): "

	// Armazena o valor de entrada na variável "nota"
	LEIA nota
	
	// Inicializa as variáveis soma e cont
	soma <- 0
	cont <- 0
	
	// Loop condicional (enquanto) executa as instruções até que a nota seja negativa
	ENQUANTO nota >= 0 FAÇA

		// Adiciona "nota" à variável "soma" a cada iteração
		soma <- soma + nota

		// Incrementa em 1 na variável "cont" a cada iteração
		cont <- cont + 1

		// Solicita a nota de outro aluno; valores negativos finalizam o loop
		ESCREVA "Digite a nota do aluno (nota negativa finaliza): "

		// Reatribui um novo valor à variável "nota"
		LEIA nota

	FIM_ENQUANTO

	// Verifica se houve alguma entrada válida de notas (cont > 0)
	SE cont > 0 ENTÃO

		// Calcula a média das notas dos alunos
		media <- soma / cont

		// Exibe a contagem de notas e a média aritmética
		ESCREVA "Foram lidas", cont, "nota(s). A média aritmética é", media

	FIM_SE

FIM_ALGORITMO
```

#### Tabela de testes

| it  | nota  | soma  | cont | nota >= 0 | soma + nota     | cont + 1 | nota    | cont > 0 | media          | saída                                            | 
| --  | --    | --    | --   | --        | --              | --       | --      | --       | --             | --                                               |
| 1   | -1.0  | 0.0   | 0    | False     |                 |          |         | False    |                |                                                  |

| it  | nota  | soma  | cont | nota >= 0 | soma + nota     | cont + 1 | nota    | cont > 0 | media          | saída                                            | 
| --  | --    | --    | --   | --        | --              | --       | --      | --       | --             | --                                               |
| 1   | 0.0   | 0.0   | 0    | True      | 0.0+0.0 = 0.0   | 0+1 = 1  | -1.0    |          |                |                                                  |
| 2   | -1.0  | 0.0   | 1    | False     |                 |          |         | True     | 0.0/1 = .0     | Foram lidas 1 nota(s). A média aritmética é 0.0! |

| it  | nota  | soma  | cont | nota >= 0 | soma + nota     | cont + 1 | nota    | cont > 0 | media          | saída                                            | 
| --  | --    | --    | --   | --        | --              | --       | --      | --       | --             | --                                               |
| 1   | 4.0   | 0.0   | 0    | True      | 0.0+4.0 = 4.0   | 0+1 = 1  | 8.0     |          |                |                                                  |
| 2   | 8.0   | 4.0   | 1    | True      | 4.0+8.0 = 12.0  | 1+1 = 2  | 6.0     |          |                |                                                  |
| 3   | 6.0   | 12.0  | 2    | True      | 12.0+6.0 = 18.0 | 2+1 = 3  | -8.0    |          |                |                                                  |
| 4   | -8.0  | 18.0  | 3    |           |                 |          |         | True     | 18.0/3.0 = 6.0 | Foram lidas 3 nota(s). A média aritmética é 6.0! |
