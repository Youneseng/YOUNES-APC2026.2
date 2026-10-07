```#include <stdio.h>

int main(void) {
    int dia = 3;
    switch (dia) {
        case 1: case 2: case 3: case 4: case 5:
            printf("Dia util\\n");  break;
        case 6: case 7:
            printf("Fim de semana\\n"); break;
        default:
            printf("Invalido\\n");
    }
    return 0;
}
```

```uso do comando switch, usado para selecionar ações com base no valor da variável dia.
Dias 1 a 5 são considerados úteis.
Dias 6 e 7 são fim de semana.
Qualquer outro valor é inválido.
```
