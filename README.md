# MIPS-like

## Ordem de Leitura
 - 17-13 RT entry 1
 - 18-22 RS entry 2
 - 23-27 RD dest 
 - 28-31 opcode

   Escreve Um 
   Le Dois
   OP RD RT RS
   Manipulação de Endereço sempre por RS
   Para Pular os Bits Desperdiçados 1aa

## OPCODES
  - 0000 : sll
  - 0001 : slr
  - 0010 : MUL
  - 0011 : ADD
  - 0100 : SUB
  - 0101 : AND
  - 0110 : OR
  - 0111 : XOR
  - 1000 : LES
  - 1001 : MulMatrix4x4 
  - 1010 : JMP
  - 1011 : B
  - 1100 :
  - 1101 : LI
  - 1110 : SW
  - 1111 : LW

    A0 = REG5
## Como o MulMatrix4x4 funciona:
### Inserção das Matrizes
O processador interpreta ambas as matrizes como cortes de registradores, sendo necessário alocar na memoria os valores e de forma que esteja Indice[ij] da primeira e depois, Indice[ij] da Segunda. Alem de que o limite de inserção e de 10 bits.

A matriz e divida por indice para um espaço de 4 bits, depois de calculado ambas as metades o resultado estará em sequencia, e dividido na memoria em partes. E importante notar que dado a restrição do tamanho da instrução sera necessario realizar o processo de multiplicação para cada indice.
