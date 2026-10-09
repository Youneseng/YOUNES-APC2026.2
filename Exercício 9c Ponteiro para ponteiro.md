```
#include <stdio.h>

int main(void) {
    int   x  = 42;
    int  *p  = &x;
    int **pp = &p;

    printf("x   = %d\n",   x);
    printf("*p  = %d\n",  *p);
    printf("**pp= %d\n", **pp);

    **pp = 100;
    printf("x apos **pp=100: %d\n", x);
    return 0;
}
```

```
Esse exemplo mostra um ponteiro para ponteiro (int **pp), ou seja, uma variável que guarda o endereço de outro ponteiro.

*p acessa o valor de x, enquanto **pp acessa o valor de x indiretamente através de dois níveis de referência.

Alterar **pp modifica x, demonstrando como ponteiros múltiplos permitem encadeamento de referências.
```
