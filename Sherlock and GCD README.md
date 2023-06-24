# Sherlock está atascado mientras resuelve un problema: Dada una matriz, A={a1,a2,...,aN}, quiere saber si existe un subconjuntode B  esta matriz que sigue a estas declaraciones:- B es un subconjunto no vacío. - No existe ningún número entero x(x>1) que divide todos los elementos de B. - No hay elementos de B que son iguales a otro.

#include <stdio.h>

int gcd(int numero1, int numero2)
{
    while (numero2 != 0)
    {
        int temporal = numero2;
        numero2 = numero1 % numero2;
        numero1 = temporal;
    }
    return numero1;
}

int main()
{
    int t;
    scanf("%d", &t);
    
    while (t--)
    {
        int numeroElementos, i, elemento, gc = 0;
        scanf("%d", &numeroElementos);
        
        for (i = 0; i < numeroElementos; i++)
        {
            scanf("%d", &elemento);
            gc = gcd(gc, elemento);
        }
        
        if (gc == 1)
            printf("YES\n");
        else
            printf("NO\n");
    }
    
    return 0;
}
