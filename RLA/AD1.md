<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Ciência da Computação <br>
**Disciplina:** Raciocínio Lógico Algorítmico <br>
**Código/Turma:** T160-60 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** 21/03/24 <br>
**Aluno(a):** Davi de Moura Pinheiro <br>
**Matrícula:** 2413105 <br>

**1a chamada (Sim/Não):** Não <br>
**2a chamada (Sim/Não):** Sim

## Questão 01 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis, $a$ e $b$, implemente e teste um algoritmo para trocar os valores atribuídos a elas.

#### Fluxograma:

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o valor de a:}}
B --> C[/0/]
C -->D{{Digite o valor de b:}}
D -->E[/1/]
E --> F[0 = 0]
F-->G[0 = 1]
G-->H[1 = 0]
H-->I{{"1=", 0}}
I -->J{{"0=", 1}}
```


### Questão 2 - Contagem
Dado um conjunto $n$ de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem $cont$ do número de alunos que foram aprovados no exame. Será considerado aprovado o aluno que tirar $nota$ 50 ou maior (no intervalo de 0 a 100).

#### Fluxograma: 

```mermaid

flowchart TD

A([INICIO]) --> B{{Digite o número de alunos: }}

B --> C[\30\]

C --> D[\cont = 0\]

D --> E[\i = 1\]

E --> F{i <= 30}

F --FALSE--> W{{Número de alunos aprovados: 18}}

W --> Z([FIM])

F --TRUE--> G{{Digite a nota do aluno, i}}

G --> H[\nota\]

H --> I{"nota >= 50 <br>E <br>nota <=100"}

I --TRUE--> J[\cont =+ 1\]

I --FALSE--> K[\i =+ 1\]

J --> K

K --LOOP--> F

```

#### Questão 3 - Soma de um conjunto de números

Dado um conjunto de $n$ números, implemente e teste um algoritmo para calcular a soma desses números. <br>
Aceite apenas $n$ maior ou igual a zero.

#### Fluxograma:

```mermaid

flowchart TD

A([INICIO]) --> B([FIM])

A([INICIO]) --> B{{"Digite a quantidade de números<br> (n >= 0):"}}

B --> C[\n\]

C --> D{n >= 0}

D --FALSE-->N{{"O valor deve ser maior ou igual a zero!"}}

N --> M([FIM])

D --TRUE--> E[/soma = 0/]

E --> F[i = 1]

F --> G{i <= n}

G --FALSE--> L{{"A soma dos numeros é, 5"}}

L --> M

G --TRUE--> H{{Digite um número: }}

H --> I[\5\]

I --> J[0+5= 5]

J --> K[i =+ 1]

K --LOOP--> G
```

## Questão 04 - Cálculo de uma série (1 ponto)

Dado um conjunto de $n$ termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

