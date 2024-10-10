# aprendendo_c
aula 15
//Relembrando laço while
    //int i=0;// i <- 0;
   // for (int i=5; i > 0;--i)
   // {

    //    printf("\n i=%d",i);

    //}
//    printf("\n Terminou com i=%d\n",i);
   // int i=0;
   // while( i < 5)
//{
    //    printf("\n i=%d",i);
    //    i++;
   // }
   // printf("\n Terminou com i=%d\n",i);
//


    //funçoes sub rotinas
   // int funcao(){ // declara uma funcao que retorna um int
  //  return 15;// valor do int retornado é 7
  //  }

    int x;// variavel global.Estyá fora de qualquer função
    //const float pi= 3.1415926535;

    void funcao()
    {
       static int x=15;// variavel local(automatica).
        x++;// incrementa a var global x.
        printf("Valor de x alterado para %d\n",x);
    }

    int fatorial (int n)
    {
        int produto = 1;
        while (n > 1)
        {
            produto *= n;
            --n;
        }
        return produto;
    }

    int main()// main é uma função retorna um int
    {
      //  int x = funcao();//invoca a função.atribui valor de retorno a x.
      //  printf("\n valor retornado = %d \n ",x);
    //  int x=5;
    //  int y= dobro(x);

     // printf("x=%d\t y= %d \n",x,y);



   //  float np1= 6.5;
    // float np2= 7.5;
    // float ms= media(np1,np2);
   //  printf("\n Media = %.2f \n",ms);
 //  x = 7;
  // funcao();
  // funcao();
  // funcao();
  // printf("\n Valor final de  x = %d",x);

   int n;
   printf("Digite um numero:");
   scanf("%d",&n);
   int fat = fatorial(n);
   printf("\n %d ! = %d \n",n,fat);
    return 0;// o valor de 0 é retornado
}
////////////////////////////////////////////////////////////////////////////////////////////////

float media(float a, float b)//função que retorna a media
   {
       return (a+b) / 2;
   }





































aula 16 //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
int global = 5; // e acessivel por todas as funcoes
 int x=5;

 void funcao1()
 {
   //  printf("\n Executando a funcao.\n");//void não retorna valor algum
     //return; // quando o tipo é void não precisa de return
    // global=10;
    // uma variavel local existe apenas enquanto uma função

   int x=25;//local
    x-=10;
    printf("\n x local = %d",x);
 }

  void funcao2()
 {
   //  printf("\n Executando a funcao.\n");//void não retorna valor algum
     //return; // quando o tipo é void não precisa de return
    // global=20;
    x+=20;
 }

 int dia()
 {//funcao dia() retorna um int
 // return 2;//valor retornado
 }





int main()//funcao principal
{
   // funcao();
   // funcao();
   // funcao();
   //int x=dia();
  // printf("\n o valor int x = %d: ",x);


    // funcao2();//aqui executa a atribuição do valor 20 à global
    // printf("\n global =%d\n", global);//Aqui imprime
    // funcao1();//aqui executa atribuição do valor 10
    // printf("\n global =%d\n", global);
    int x=30;// x global igual a 30
    funcao1();
    printf("\n x=%d \n",x);
   // x+=30;
   // funcao2();
   // printf("\n x=%d \n",x);

    return 0;
}



aula 16_01   //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////




// a função soma recebe dois parametros do tipo int.
//parametros a e b. na verdade são duas variaveis que contém
// o valor dos argumentos durante a invocação.
  //int soma(int a,int b)
 //{
  //  return a+b;//retorna a soma dos parâmetros a e b.
//  }

//int mult(int a,int b)
//{
 //   return a * b;
//}

//int sub(int a,int b)
//{
 //   return a - b;
//}

int soma_acumulativa (int n)
{
    int soma=0;// variavel soma inicia com zero
    for (int i=1; i <= n;i++)//para os numeros de 1 até n;
    {
        soma += i;//adiciona o valor i a variavel soma

    }
    return soma;//retorna o valor da variável soma.

}

int fatorial (int n)
{
    int produto=1;// o fatorial começa com 1.
    for (int i=1; i <= n;i++)
    {
        produto *= i;
    }
    return produto;
}





int main()//main() retorna int e é a função principal
{

   // int x;
    //printf("Digite o valor do limite:");
   // scanf("%d",&x);
   // int y = soma_acumulativa(x);
   // printf("\n Soma acumulada = %d \n",y);
    int x;
    printf("Digite o valor a ser fatorado:");
    scanf("%d",&x);
    int y = fatorial(x);
    printf("\n fatorial e = %d \n",y);
  //  int x=20;
  //  int y=5;
  //  int z = soma(x,y);
   // printf("\n soma = %d\n",z);
  //  int i = sub(x,y);
  //  printf("\n sub = %d\n",i);
  //  int v = mult(x,y);
  //  printf("\n mult = %d\n",v);
//
    return 0;
}





///////////////////////// aula 17 

aula 17 
void funcao( int profundidade ) // funcao recursiva
{
    // (char x ,int y)
    //int a = 5 + x;
    //int b = 6 - y;
    //int c = a + b;
   // printf("\n %d",c);
   if (profundidade < 0)
   {
       return;
   }
   printf("\n profundidade = %d ",profundidade);
   funcao(profundidade - 1);// funcao() invoca a si mesma.

}
int main()
{
    // funcao(5,8);
    funcao(8);
    return 0;



}


aula 17_01
int fatorial(int n)
{
   // int produto= 1;
   // while (n > 1)
   // {
    //    produto*= n;
    //    --n;
   // }

   return n > 1 ? n * fatorial(n -1):1;

   if (n < 2)
   {
       return 1;
   }
   else
   {
       return n * fatorial(n -1);
   }



   // if (n < 2){return 1;}
   // while(n)
   // {
    //    produto*=n;
   //     --n;
  ///  }
  ////////////////////////////
   // for(int i = 1; i <= n; i++)
  //  {
   //     produto *= i;
  //  }
//    return produto;

}

int main()
{
    //int x=5;
   // int y= fatorial(x);
    for(int x=0;x<12;x++)
    {
        int y=fatorial(x);
          printf("\n %d ! = %d \n", x,y);
    }


    return 0;
}




//////////////////////////////////////////

aula 17_02
int main()
{

 int vetor[3];

 vetor[0]= 5;
 vetor[1]= 3;
 vetor[2]= 4;
 
 printf("\n vetor[0] = %d", vetor[0]);
printf("\n vetor[1] = %d", vetor[1]);
printf("\n vetor[2] = %d", vetor[2]);

    return 0;
}



////////////////////////////////////

aula 17_03



int main()
{

 int vetor[3];

 //vetor[0]= 5;
 //vetor[1]= 3;
 //vetor[2]= 4;
 for (int i=0;i<3;i++)
 {
     int valor;
     printf("\n Digite o valor do elemento de indice %d: ",i);
     scanf("%d",&valor);
     vetor[i]=valor;
 }
 for(int i=0;i<3;i++)
 {
     printf("\n vetor[%d]=%d",i,vetor[i]);
 }

// printf("\n vetor[0] = %d", vetor[0]);
//printf("\n vetor[1] = %d", vetor[1]);
//printf("\n vetor[2] = %d", vetor[2]);

    return 0;
}


//////////////////////////////
aula 18

int main()
{
   //vetor de 5 elementos do tipo int.
   // os índices variam de 0 a 4.
   int vetor[5];

   vetor[0]=8;
   vetor[1]=7;
   vetor[2]=4;
   vetor[3]=2;
   vetor[4]=1;//ultimo elemento
   //exibe na sequencia inversa



  // for (int indice=0;indice < 5;indice++)
  // {
   // printf("\n vetor[%d]= %d \n",indice,vetor[indice]);
   //}

   /*  for (int indice=4;indice > -1;indice--)
   {
    printf("\n vetor[%d]= %d \n",indice,vetor[indice]);
   }
   */

///////////////////////////////////////

   aula 18_02


   int main()
{
   int vetor[NUM_ELEMENTOS];
   // OS indices variam de 0 a num_elementos - 1
  // vetor[0]=8;
  // vetor[1]=7;
   //vetor[2]=4;
   //vetor[3]=2;
   //vetor[4]=1;
   //vetor[5]=-10;
   for (int indice=0; indice < NUM_ELEMENTOS;indice++)
   {
       int valor;
       printf("\n Digite o valor do vetor[%d]:",indice);
       scanf("%d",&valor);
       vetor[indice]=valor;
   }

   printf("\n Exibindo os valores fornecidos: \n");


   for (int indice=0;indice < NUM_ELEMENTOS;indice++)
   {
    printf("\n vetor[%d]= %d \n",indice,vetor[indice]);
   }

    return 0;
}



///////////////////////////// 18_03

int main()
{
  float vetor[NUM_ELEMENTOS];
   // OS indices variam de 0 a num_elementos - 1
  // vetor[0]=8;
  // vetor[1]=7;
   //vetor[2]=4;
   //vetor[3]=2;
   //vetor[4]=1;
   //vetor[5]=-10;
   for (int indice=0; indice < NUM_ELEMENTOS;indice++)
   {
       float valor;
       printf("\n Digite o valor do vetor[%d]:",indice);
       scanf("%f",&valor);
       vetor[indice]=valor;
   }

   printf("\n Exibindo os valores fornecidos: \n");


   for (int indice=NUM_ELEMENTOS - 1;indice >= 0;indice--)
   {
    printf("\n vetor[%d]= %.2f \n",indice,vetor[indice]);
   }

    return 0;
}


////////////////////////
aula 18_03

//função recebe um valor de caractere como parametro
int numeroDeCaracteres(char texto[])
{


 int contador = 0;
    while(texto[contador] != '\0')
    {
        ++contador;
    }

    return contador;
    }


int main()
{

   char texto[50];
   printf("Digite algo:");
   gets(texto);
   int comprimento = numeroDeCaracteres(texto);
   printf("\n A string:\n %s \n possui %d caracteres.",texto,comprimento  );

   printf("\n Exibindo os caracteres em ordem inversa:\n");
   for(int i= comprimento-1; i >= 0;i--)
   {
       printf("%c",texto[i]);
   }
   printf("\n\n");
    return 0;
 // printf("Voce digitou: \n %s \n",texto);

  // char texto[50]= "Agora sim "; //{'0','i','!','\0'};// char é um texto de 50 caracteres
  // texto[5]='\0';// caractere da posição 5 virou nulo

 // int indice=0;
 // while(texto[indice] != '\0')
 // {
   //   printf("\n %c",texto[indice]);
   //   indice++;

  //}
 // for (int indice=0;texto[indice] != '\0';indice++)
 // {
     // printf("\n %c",texto[indice]);
 // }

  // printf("%s",texto);//para exibir string use $s]]

 // char texto[50];
  //printf("Digite algo:");
 // gets(texto);
 // printf("Voce digitou: \n %s \n",texto);
 //int contador = 0;
 //while(texto[contador] != '\0')
 //{
  //   ++contador;
 //}


}





