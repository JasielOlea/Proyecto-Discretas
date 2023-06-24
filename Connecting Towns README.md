# Las ciudades en un mapa están conectadas por varias carreteras. El número de carreteras entre cada ciudad 
# está en una matriz y la ciudad 0 es la ubicación de partida. El número de caminos desde la ciudad 0a la ciudad 1
# es el primer valor de la matriz, de la ciudad 1 a la ciudad 2 es el segundo, y así sucesivamente.
# ¿Cuántos caminos hay desde la ciudad? 0 hasta la última ciudad de la lista, módulo 1234567?

#include <stdio.h>

int main() {
    int x;
    scanf("%d", &x);
    
    int numero_casos = 1;
    while (numero_casos <= x) {
        int cantidad_numeros;
        scanf("%d", &cantidad_numeros);
        
        int resultado= 1;
        int i = 1;
        while (i < cantidad_numeros) {
            int numero;
            scanf("%d", &numero);
            resultado = (numero * resultado) % 1234567;
            i++;
        }
        
        printf("%d\n", resultado);
        
        numero_casos++;
    }
    
    return 0;
}
