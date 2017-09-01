# Jogo-da-forca
Jogo em desenvolvimento para a nota final do 1º período do curso.

#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <locale.h>

int main(){
setlocale(LC_ALL, "portuguese");

    char banco[11][16] = {
        "acatado","aprovado", "amigo", "pessoal",
        "estagnada", "afrodescendente","negro",
        "antagônico", "contrário", "adesão",
        "apoio"
    };

    char PALAVRAS [10];
    int aleatorio=0, i;    

    srand(time(NULL));

    aleatorio = rand() % 11;

    //Copiar a linha da matriz para o vetor
    for (i=0; i<10; i++){
        PALAVRAS[i]= banco[aleatorio][i]; 
        /** 'aleatório' vai ser a linha do vetor (a palvra aleatoria) e 'i' vai ser a
        quantidade de caracteres*/
    }

    printf("\n\n\n%s\n\n", PALAVRAS);

    printf("\n _ _ _ _ _ _ _ _\n\n\n");




    system("pause");
    return 0;
}
