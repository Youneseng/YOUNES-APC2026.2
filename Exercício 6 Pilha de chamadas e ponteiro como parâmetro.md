```
#include <stdio.h>

int fatorial(int n) {
    if (n <= 1) return 1;
    return n * fatorial(n - 1);
}

void dobra(int *x) { *x *= 2; }

int main(void) {
    printf("5! = %d\n", fatorial(5));

    int v = 7;
    dobra(&v);
    printf("dobro de 7 = %d\n", v);

    /* ponteiro para função */
    int (*fn)(int) = fatorial;
    printf("fn(4) = %d\n", fn(4));   /* 24 */
    return 0;
}
```

```
O programa define uma função recursiva fatorial, que chama a si mesma até atingir o caso base (n <= 1). 
Isso exemplifica o uso da pilha de chamadas: cada chamada fica empilhada até retornar.

A função dobra mostra como passar ponteiros como parâmetro: ao receber int *x, ela altera diretamente o valor da variável original.

Também há um exemplo de ponteiro para função, permitindo armazenar a referência de fatorial em fn e chamá-la como se fosse uma função normal.
```
