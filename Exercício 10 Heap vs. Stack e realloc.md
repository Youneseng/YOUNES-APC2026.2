```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int n = 4;
    int *v = calloc(n, sizeof(int));   /* heap, inicializado com 0 */
    if (!v) { perror("calloc"); return 1; }

    for (int i = 0; i < n; i++) v[i] = (i + 1) * 10;
    for (int i = 0; i < n; i++) printf("v[%d]=%d\n", i, v[i]);

    /* expandir para 6 elementos */
    n = 6;
    int *tmp = realloc(v, n * sizeof(int));
    if (!tmp) { free(v); perror("realloc"); return 1; }
    v = tmp;
    v[4] = 50; v[5] = 60;
    for (int i = 0; i < n; i++) printf("v[%d]=%d\n", i, v[i]);

    free(v);
    v = NULL;
    return 0;
}
```

```
O programa mostra como alocar memória dinâmica na heap usando calloc, que inicializa os valores com zero.

Depois, expande o bloco com realloc, permitindo aumentar o tamanho do array sem perder os dados já armazenados.

Isso contrasta com variáveis locais na stack, que têm tamanho fixo e vida limitada ao escopo da função.

Finaliza liberando a memória com free, prática essencial para evitar vazamentos.
```
