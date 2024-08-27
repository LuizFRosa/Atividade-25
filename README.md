# Atividade-25

#include <stdio.h>  // Inclui a biblioteca padrão de entrada e saída

#define MAX_BITS 64  // Define o tamanho máximo do número binário

int main() {
    unsigned long long decimalNum;
    char binario[MAX_BITS + 1];  // Array para armazenar a representação binária
    int i = 0;

    // Solicita ao usuário que insira um número decimal
    printf("Digite um numero decimal: ");
    scanf("%llu", &decimalNum);  // Lê o número decimal fornecido pelo usuário

    // Verifica se o número é zero
    if (decimalNum == 0) {
        printf("O binario equivalente e: 0\n");
        return 0;  // Encerra o programa com sucesso
    }

    // Converte o número decimal para binário
    while (decimalNum > 0) {
        binario[i++] = (decimalNum % 2) + '0';  // Obtém o resto da divisão por 2 e converte para caractere
        decimalNum /= 2;  // Divide o número decimal por 2
    }

    binario[i] = '\0';  // Adiciona o caractere nulo ao final do array

    // Exibe o número binário em ordem inversa
    printf("O binario equivalente e: ");
    for (int j = i - 1; j >= 0; j--) {
        printf("%c", binario[j]);
    }
    printf("\n");

    return 0;  // Indica que o programa terminou com sucesso
}
