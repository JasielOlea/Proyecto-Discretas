# Una persona se está preparando para irse y necesita un par de calcetines a juego. Si hay n colores de los calcetines en el cajón, ¿cuántos calcetines se deben quitar para estar seguro de tener un par que haga juego?

#include <stdio.h>

int main() {
    int x;
    scanf("%d", &x);
    
    for (int i = 0; i < x; i++) {
        int n;
        scanf("%d", &n);
        
        int resultado = n + 1;
        printf("%d\n", resultado);
    }
    
    return 0;
