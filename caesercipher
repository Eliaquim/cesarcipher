#include <stdio.h>
#include <cs50.h>
#include <ctype.h>
#include <string.h>
#include <stdlib.h>

char alterar(char letra, int maiscouminusc);

int k;

int main(int argc, string argv[])
{
    // initialized just because the compiler "asked"
    string original = 0;

    // work only with 2 arguments, no more, no less
    if (argc < 2 || argc > 2)
    {
        printf("Uso: ./caeser k, onde k é um número\n");
        return 1;
    }
    else
    {
        // check that arguments where passed
        if (argv[1] != NULL)
        {
            // turns the number into an integer type
            k = atoi(argv[1]);
            // prompt the user for a name
            original = get_string("Texto para encriptar: ");
        }
    }

    printf("Texto encriptado: ");

    for (int i = 0, comprim = strlen(original); i < comprim; i++)
    {
        if (isalpha(original[i]))
        {
            char letra = original[i];
            if (islower(letra))
            {
                // shift with function for lower case (97)
                char encriptado = alterar(letra, 97);
                printf("%c", encriptado);
            }
            else
            {
                // shift with function for upper case (65)
                char encriptado = alterar(letra, 65);
                printf("%c", encriptado);
            }
        }
        else
        // print the character intact if it is not alphanumeric
        {
            printf("%c", original[i]);
        }
    }
    printf("\n");
}

char alterar(char letra, int maiscouminusc)
{
    char indicealfanum = letra - maiscouminusc;
    char indicealfanumcomchave = (indicealfanum + k) % 26;
    char encriptado = indicealfanumcomchave + maiscouminusc;

    return encriptado;
}
