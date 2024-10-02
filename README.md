# aprendendo_c

aula 16

 void funcao()
 {
     printf("\n Executando a funcao.\n");//void não retorna valor algum
     //return; // quando o tipo é void não precisa de return
 }

 int dia()
 {//funcao dia() retorna um int
  return 2;//valor retornado
 }





int main()//funcao principal
{
   // funcao();
   // funcao();
   // funcao();
   int x=dia();
   printf("\n o valor int x = %d: ",x);

    return 0;
}
