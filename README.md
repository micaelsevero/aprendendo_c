# aprendendo_c

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

