#include <stdio.h>
#include <stdlib.h>

	struct pes{
		char nome[50];
		char rua[20];
		char sexo;
	};

struct ang{
	struct pes avalia;
	int idade;
	char *saude;
}op;

void acess(struct pes *f);
int main(int argc, char *argv[])
{
	struct pes ap;
	
	puts("Insira seus dados pessoais:");
	gets(&ap.nome);
	gets(&ap.rua);
	gets(&ap.sexo);
	acess(&ap);
	puts("\nNova estrutura:");
	op.avalia.sexo = 'F';
	op.idade = 22;
	op.saude = "Indefinido";
	printf("\n%c\n%d\n%s",op.avalia.sexo,op.idade,op.saude);
	return 0;
}

void acess(struct pes *f)
{
	if(f == NULL)
	{
		puts("Erro!");
		exit(1);
	}
	printf("%s\n",f->nome);
	printf("%s",f->rua);
	printf("\n%c",f->sexo);
}
