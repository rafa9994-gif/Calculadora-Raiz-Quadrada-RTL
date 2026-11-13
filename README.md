Projeto de Unidade Lógico-Aritmética (ULA) e Decodificador 7 Segmentos
🎯 Objetivo do Projeto
Desenvolver uma Unidade Lógico/Aritmética (ULA) para processamento de operandos de 5 bits, integrada a um decodificador binário projetado para acionar displays de sete segmentos.

Este projeto foi construído focado no baixo nível de hardware, utilizando exclusivamente diagramas de blocos com portas lógicas básicas (AND, OR, XOR, etc). Nenhum componente de alto nível ou linguagem de descrição de hardware (como VHDL) foi utilizado, exigindo que até mesmo os multiplexadores fossem construídos do zero.

⚙️ Principais Funcionalidades
Processamento Binário: O sistema foi modelado para processar números binários positivos e negativos formatados em complemento a 2.
Decodificador Integrado: Um circuito decodificador acoplado converte a saída de 5 bits da ULA para dois vetores de 7 bits, alimentando os displays numéricos.
Sinalizadores de Estado (Flags): Implementação de saídas para LEDs indicadores de:
Overflow (1 bit): Indica transbordo em operações.
Status (1 bit): Retorna verdadeiro/falso para operações booleanas.
Sinal (1 bit): Acende para indicar que o resultado numérico é negativo.
🧮 Tabela de Operações da ULA
A ULA executa as seguintes funções, controladas por um vetor seletor S de 3 bits:

Seleção (S2 S1 S0)	Operação / Função Executada
0 0 0	F = A + B (Soma)
0 0 1	F = A - B (Subtração)
0 1 0	F = MAX(A, B) (Maior valor)
0 1 1	F = 0; Status = (A <= B)
1 0 0	F = 0; Status = 1 se A for par (0 caso contrário)
1 1 0	F = |A - B| (Valor absoluto da subtração)
1 1 1	F = A * 3 (Multiplicação por constante)
🛠️ Tecnologias e Conceitos Aplicados
Sistemas Digitais e Eletrônica Digital
Lógica Combinacional pura
Arquitetura de Hardware e Diagrama de Blocos
Matemática Binária (Complemento a 2)
