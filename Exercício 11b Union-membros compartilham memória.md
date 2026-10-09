```
#include <stdio.h>

union Dado { int i; float f; char c; };

int main(void) {
    union Dado d;
    d.i = 65;
    printf("d.i='%d'  d.c='%c'\n", d.i, d.c);   /* 65 e 'A' — mesmos bytes */
    d.f = 3.14f;
    printf("d.f=%.2f\n", d.f);   /* d.i agora tem valor indefinido */
    return 0;
}
```

```
Uma union permite que diferentes membros compartilhem o mesmo espaço de memória.

Aqui, d.i e d.c ocupam os mesmos bytes, então atribuir 65 a i faz com que c seja interpretado como 'A'.

Quando d.f recebe um valor, os outros membros ficam indefinidos, pois todos compartilham a mesma área.

É útil para representar dados que podem assumir diferentes formatos, mas nunca simultaneamente.
```
