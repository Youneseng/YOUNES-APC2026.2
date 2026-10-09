```
#include <stdio.h>

int main(void) {
    int x = 10;
    int *p = &x;

    printf("x    = %d\n",  x);
    printf("&x   = %p\n",  (void*)&x);
    printf("p    = %p\n",  (void*)p);
    printf("*p   = %d\n",  *p);

    *p = 99;
    printf("x apos \*p=99: %d\n", x);
    return 0;
}
```

```
O programa mostra o conceito de ponteiro: p guarda o endereço da variável x.

*p é a derreferência, ou seja, acessar o valor armazenado no endereço.

Ao fazer *p = 99, o valor de x é alterado diretamente, mostrando que ponteiros permitem manipular variáveis por referência.
```
