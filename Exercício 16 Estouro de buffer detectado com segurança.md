```
#include <stdio.h>
#include <string.h>

int main(void) {
    char destino[8];

    /* SEGURO: limita a cópia ao tamanho do buffer */
    strncpy(destino, "Brasilia-DF", sizeof(destino) - 1);
    destino[sizeof(destino) - 1] = '0';   /* garante terminador */

    printf("destino = '%s'\n", destino);   /* "Brasili" */
    printf("strlen  = %zu\n",  strlen(destino));   /* 7 */

    /* ALTERNATIVA SEGURA com snprintf */
    char buf[16];
    int  n = snprintf(buf, sizeof(buf), "valor=%d", 12345);
    if (n >= (int)sizeof(buf)) printf("truncado!\n");
    printf("buf = '%s'\n", buf);
    return 0;
}
```

```
O código demonstra como evitar estouro de buffer ao copiar strings: strncpy limita a quantidade de bytes copiados ao tamanho do array.

O terminador '\0' é garantido manualmente, já que strncpy pode não colocá‑lo se houver truncamento.

A alternativa com snprintf é ainda mais segura: ela nunca escreve além do limite e informa se houve truncamento.

Mostra boas práticas de manipulação de strings em C, onde o programador deve sempre controlar o tamanho do buffer.
```
