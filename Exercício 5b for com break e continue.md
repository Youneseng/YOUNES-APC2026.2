```
#include <stdio.h>

int main(void) {
    for (int i = 0; i < 10; i++) {
        if (i % 2 == 0) continue;
        if (i == 7)     break;
        printf("%d\\n", i);
    }
    return 0;
}
```

```laço for que percorre valores de 0 a 9.
O comando continue faz o loop “pular” os números pares (não imprime).
O comando break interrompe o loop quando i == 7.
Assim, o programa imprime apenas os números ímpares menores que 7. É um exemplo de controle de fluxo dentro de laços.
```
