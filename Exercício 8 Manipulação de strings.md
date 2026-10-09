```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(void) {
    char s[] = "Brasilia";
    printf("Comprimento: %zu\n", strlen(s));

    for (int i = 0; s[i] != '\0'; i++)
        printf("s[%d]='%c' ASCII=%d\n", i, s[i], (int)s[i]);

    /* comparação */
    printf("strcmp: %d\n", strcmp(s, "Brasilia"));    /* 0 */
    printf("strcmp: %d\n", strcmp(s, "Curitiba"));    /* negativo */

    /* busca */
    char *pos = strchr(s, 'i');
    if (pos) printf("Primeiro 'i' na posição %td\n", pos - s);  /* 5 */

    /* conversão */
    int n = atoi("1234");
    printf("atoi(\"1234\") = %d\n", n);
    return 0;
}
```

```
Trabalha com strings em C, que são arrays de caracteres terminados por '\0'.

Usa strlen para medir o comprimento e percorre cada caractere mostrando seu valor ASCII.

Demonstra comparação de strings com strcmp, que retorna 0 quando iguais e valores negativos/positivos quando diferentes.

Usa strchr para buscar um caractere dentro da string, retornando um ponteiro para a posição encontrada.

Mostra conversão de string para número com atoi, transformando "1234" em inteiro.
```
