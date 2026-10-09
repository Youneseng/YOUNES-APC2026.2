```
#include <stdio.h>

int main(void) {
    int nota = 72;
    if      (nota >= 90) printf("A\\n");
    else if (nota >= 80) printf("B\\n");
    else if (nota >= 70) printf("C\\n");
    else                 printf("Reprovado\\n");
    return 0;
}
```
```
o uso das estruturas condicionais if/else if/else para classificar uma nota em conceitos (A, B, C ou Reprovado). Ele compara o valor da variável nota com limites e imprime o resultado correspondente. É um exemplo clássico de decisão baseada em faixas de valores.
```
