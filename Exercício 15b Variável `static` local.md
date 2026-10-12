```
#include <stdio.h>

void contador(void) {
    static int n = 0;   /* inicializado UMA VEZ; persiste entre chamadas */
    n++;
    printf("chamada %d\n", n);
}

int main(void) {
    contador(); contador(); contador();   /* 1, 2, 3 */
    return 0;
}
```

```
A variável static dentro da função é inicializada apenas uma vez e mantém seu valor entre chamadas.

Isso permite criar funções com “memória interna”, como contadores, acumuladores ou estados persistentes.

Cada chamada incrementa n, mostrando que o valor não é reinicializado como ocorre com variáveis locais comuns.
```
