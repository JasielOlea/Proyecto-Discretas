# A Kristen le encanta jugar y comparar números. Ella piensa que si toma dos números positivos diferentes, aquel cuyos dígitos suman un número mayor es mejor que el otro. Si la suma de los dígitos es igual para ambos números, entonces piensa que el número más pequeño es mejor. Por ejemplo, Kristen piensa que 13 es mejor que 31 y eso 12 es mejor que 11. Dado un número entero,n, puedes encontrar el divisor de n que Kristin considerará la mejor?

#include<iostream>
#include<stdlib.h>
using namespace std;

int main(){
    int numero;
    cin>>numero;
    int numMaximo=0;
    int sumaNumeros=0;
        for (int i = 1; i <= numero; i++) {
        if (numero % i == 0) {
            int contador = 0;
            int casosNumeros = i;

            while (casosNumeros!= 0) {
                contador = contador + casosNumeros % 10;
                casosNumeros = casosNumeros / 10;
            }

            if (contador > numMaximo) {
                numMaximo = contador;
                sumaNumeros = i;
            }
        }
    }
    cout<<sumaNumeros;
    return 0;
}
