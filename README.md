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




/ a função soma recebe dois parametros do tipo int.
//parametros a e b. na verdade são duas variaveis que contém
// o valor dos argumentos durante a invocação.
int soma(int a,int b)
{
    return a+b;//retorna a soma dos parâmetros a e b.
}

int mult(int a,int b)
{
    return a * b;
}

int sub(int a,int b)
{
    return a - b;
}



int main()//main() retorna int e é a função principal
{
    int x=20;
    int y=5;
    int z = soma(x,y);
    printf("\n soma = %d\n",z);
    int i = sub(x,y);
    printf("\n sub = %d\n",i);
    int v = mult(x,y);
    printf("\n mult = %d\n",v);

    return 0;
}

