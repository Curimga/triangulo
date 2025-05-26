# triangulo
#include <stdio.h>
#include <stdlib.h>

int main () {
    int a, b, c;
    
    printf("Digite o valor do lado a: ");
    if (scanf("%d", &a) != 1 || a <= 0) {
        printf("Entrada invalida! O lado A deve ser maior do que 0\n");
        return 1;
    }
    
    printf("Digite o valor do lado b: ");
    if (scanf("%d", &b) != 1 || b <= 0) {
        printf("Entrada invalida! O lado B deve ser maior do que 0\n");
        return 1;
    }
    
    printf("Digite o valor do lado c: ");
    if (scanf("%d", &c) != 1 || c <= 0) {
        printf("Entrada invalida! O lado C deve ser maior do que 0\n");
        return 1;
    }

    // Verificação se os lados formam um triângulo
    if (a < b + c && b < a + c && c < a + b) {
        printf("Estes lados formam um triângulo.\n");

        // Classificação do triângulo
        if (a == b && b == c) {
            printf("Triângulo equilátero.\n");
        } else if (a == b || a == c || b == c) {
            printf("Triângulo isósceles.\n");
        } else {
            printf("Triângulo escaleno.\n");
        }

    } else {
        printf("Estes lados NÃO formam um triângulo.\n");
    }

    return 0;
}
