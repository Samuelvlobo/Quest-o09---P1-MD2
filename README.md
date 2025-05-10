(PARTE 2)

QUESTÃO 9 ( 1,5 ponto)

Um estudante está desenvolvendo uma função de segurança para validar acessos em um sistema. Essa função baseia-
se na ideia de "verificação modular", utilizando os conceitos de congruência, primalidade, coprimalidade, Pequeno

Teorema de Fermat, Teorema de Euler e exponenciação modular eficiente.
Porém, o sistema da escola do professor utiliza um método especial para definir a base da potência. Ao invés desta
fornecida diretamente, o valor da base a é definido como o resultado da divisão modular entre dois elementos de
Zn
(Ex: 38⊘79 em Z252 , generalizando: H⊘G em Zn
)

Implemente um programa em C que tenha:
Dados de entrada
• três números inteiros positivos H, G e n, usados para calcular a base a
• um expoente x
• um módulo n1
CALCULAR: a
xmod n1
Etapas que o programa deve realizar:
1. Verificar se G e n são primos utilizando o Algoritmo de Euclides
* se não forem, justificar que a divisão não é possível
2. Calcular o inverso de G em Zn

utilizando divisões sucessivas

* se G
−1
não pertencer a Zn

verificar equivalência

3. Dividir H por G e encontrar a
4. Verificar se a e n1

são coprimos.

5. Verificar se n1
é primo.

6. Se n1

for primo, aplicar o Pequeno Teorema de Fermat, e definir x1=n−1 .
7. Caso contrário, aplicar o Teorema de Euler, e definir x1=φ(n) (função totiente de Euler)

*Implemente a função φ(n1

) sem usar bibliotecas prontas, apenas com base nos fatores primos de

n1
.
8. Utilizar o teorema da divisão para decompor o expoente x na forma x=x 1∗q+r .
9. Reescrever a expressão a
xmod n1
como: a
x≡(((a
x 1
)
qmod n1
)⋅(a
rmod n1
))mod n1

10.Calcular os seguintes valores intermediários:
• a
x1mod n1=x 2
• x2
qmod n1
• a
r mod n1

11.Combinar os resultados e imprimir o valor final da congruência: ((x2
q
)⋅(a
r
))mod n1

OBJETIVO:
Permitir que o programa execute todas as etapas acima e imprima os passos de forma clara, educativa e detalhada,
como em uma explicação matemática.
