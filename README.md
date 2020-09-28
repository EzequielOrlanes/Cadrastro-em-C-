#include <stdio.h>
#include <stdlib.h>
#include <string.h>


struct cadastro{
char nome[50];
int idade;
float salario;
};
//Estrutura que vai armazenar os dados de uma pessoa,
// vai utilizada abaixo para armazenar quantos dados forem necessários na função main

int main()
{ int i=0, y=0;
char aux[8];//colhe o comando do usúario
char inserir[8]= "inserir";// palavras chave que vão dar comandos ao programa
char mostrar[8]= "mostrar";
char sair[5]="sair";

////CONTADORES///
int contador=0;
int contador_procura=0;


char nome_procurado[50];//caso a opção seja mostra -> armazena o nome procurado
struct cadastro pessoa[4];
//declaração da estrutura que tá logo acima


                                      inicio:  //usado para criar um "loop" , para que o programa após fazer um cadrastro consiga realizar
    scanf("%s",aux);
///////////
if (aux!=sair ){
    if(strcmp(aux,inserir)==0)
 { if( contador<4){
    //printf("Insira seu nome?");
scanf("%s %d %f",pessoa[i].nome,&pessoa[i].idade,&pessoa[i].salario);

printf("Registro %s %d %0.2f inserido\n",pessoa[i].nome,pessoa[i].idade ,pessoa[i].salario); //imprimi o registro daquela posição

   contador++;
               i++;
                    goto inicio;
                        }

  else {scanf("%s %d %f");
  printf("Espaço insuficiente\n"); goto inicio; }///campo de verificação se há espaço na lista
 }

 else if(strcmp(aux,mostrar)==0)
    {
        //printf("insira o nome da pessoas que deseja encontrar?");
        scanf("%s",nome_procurado);

for(y=0;y<4;y++)
{ if(strcmp(pessoa[y].nome,nome_procurado)== 0)
     { printf("Registro %s %d %0.2f\n",pessoa[y].nome,pessoa[y].idade ,pessoa[y].salario);
     goto inicio;
           }
           else {  contador_procura++;      /*printf("Registro ausente\n"); goto inicio;*/}
              }

              if(contador_procura == 4)
              {printf("Registro ausente\n"); goto inicio;}
    }




} else{ return 0;}


}
