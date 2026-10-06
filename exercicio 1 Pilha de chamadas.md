```
#include <stdio.h>

int mult(int a, int b) {
    return a * b;
}

int soma_mult(int a, int b, int c) {
    return a + mult(b, c);
}

int main(void) {
    int resultado = soma_mult(1, 5, 3);
    printf("%d\n", resultado);   /* 16 */
    return 0;
}
```

```
o codigo demonstra definição de funções, passagem de parâmetros por valor e chamada de função dentro de outra função. mult é chamada dentro de soma_mult, mostrando composição de funções.
```
