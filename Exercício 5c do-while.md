´´´
#include <stdio.h>

int main(void) {
    int n = 1;
    do {
        printf("n = %d\\n", n);
        n *= 2;
    } while (n < 32);
    return 0;
}
´´´

´´´
Esse código usa um laço do...while, que garante pelo menos uma execução antes da verificação da condição. 
A variável n começa em 1 e é multiplicada por 2 a cada passo, imprimindo os valores até ser menor que 32. 
É um exemplo de loop com multiplicação progressiva.
´´´
