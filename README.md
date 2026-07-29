# Projeto RTL: Calculadora de Raiz Quadrada Inteira

## 🎯 Objetivo do Projeto
Desenvolver um circuito digital capaz de calcular a raiz quadrada inteira de um número de 8 bits. O cálculo matemático foi implementado utilizando o método de subtrações sucessivas de números ímpares, descartando a necessidade de usar blocos complexos de divisão ou multiplicação em hardware.

O projeto foi inteiramente fundamentado na **Metodologia RTL (Register-Transfer Level)**, dividindo o sistema em Bloco Operacional (Datapath) e Bloco de Controle (FSM).

## ⚙️ Especificações e Arquitetura
* **Entradas:** 
  * `N`: Vetor de 8 bits representando o número a ser processado.
  * `comece`: Sinal de 1 bit para iniciar a operação.
* **Saídas:**
  * `raiz`: Vetor de 4 bits contendo o resultado final.
  * **Interface:** Exibição do resultado (raiz) integrada a um display de 7 segmentos.
* **Bloco Operacional (Datapath):** Implementado em esquemático, contendo os registradores de 8 bits (`a` e `subtraendo`) e o registrador de 4 bits (`raiz`).
* **Bloco de Controle (FSM):** Máquina de estados responsável por gerenciar as operações condicionais e o laço de repetição do algoritmo, desenvolvida em VHDL.

## 🧠 Algoritmo de Hardware Implementado
A lógica sequencial projetada segue o fluxo de estados abaixo:
1. Aguarda o sinal de `comece`.
2. Copia o valor da entrada (`a = N`), inicializa o `subtraendo = 1` e a `raiz = 0`.
3. Em loop (enquanto `a >= subtraendo`), o circuito executa:
   * `a = a - subtraendo`
   * `subtraendo = subtraendo + 2`
   * `raiz = raiz + 1`

## 🛠️ Tecnologias e Metodologia
* **Sistemas Digitais** e Eletrônica Digital
* **Metodologia RTL** (Register-Transfer Level)
* **FSM e FSMD** (Máquinas de Estados de Baixo e Alto Nível)
* **VHDL** (para o bloco de controle)
* Arquitetura de Hardware baseada em Esquemáticos
