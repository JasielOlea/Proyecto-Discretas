# Watson da un número entero N a Sherlock y le pregunta: 
# ¿Cuál es el número de divisores de N que son divisibles por 2?.
#include <stdio.h>

int main() {
    int t;
    scanf("%d", &t);

    while (t--) {
        long long numero;
        long long divisores_pares =0;
        
        scanf("%lld", &numero);

        long long i = 1;
        while (i * i < numero) {
            if (numero % i == 0) {
                divisores_pares += (i % 2 == 0) + ((numero / i) % 2 == 0);
            }
            i++;
        }

        if (i * i == numero && i % 2 == 0)
            divisores_pares++;

        printf("%lld\n", divisores_pares);
    }

    return 0;
}
