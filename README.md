# MeusEstudosEmC
Linguagem C


//**Um comerciante comprou um produto e deseja revendê-lo com um lucro de
45% se o valor de compra for menor do que R$ 20,00; caso contrário, o lucro
será de 30%. Entrar com o valor de compra do produto e exibir seu valor de
venda.**//

#include <stdio.h>
#include <stdlib.h>

int main(){
    float prod,vend;
    printf("informe o valor da compra:\n");
    scanf("%f",&prod);
     if(prod < 20){
        vend=prod+(prod*0.45);
        printf("valor da venda: %f", vend);
     }
     else {
            vend=prod+(prod*0.30);
            printf(" valor da venda: %f", vend);

     }

    return 0;
}




//**2 - Dado o salário bruto de uma pessoa, exibir o desconto do INSS segundo a
tabela abaixo e exibir o valor a receber:**//

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(){
	
	float salario, desconto, sal_receber;
	
	printf("Digite o valor do salario: ");
	scanf("%f", &salario);
	
	if(salario <= 600){
		printf("Isento do desconto e o valor a receber e de %.2f\n", salario);
	}
	else if(salario > 600 && salario < 1200){
		
		desconto = salario * 0.2;
		sal_receber = salario - desconto;
		
		
		printf("O valor do desconto e de %.2f\n", desconto);
		printf("O valor do salario a receber e de %.2f\n", sal_receber);
		
	}
	else if(salario > 1200 && salario <=2000){
		
		desconto = salario * 0.25;
		sal_receber = salario - desconto;
		
		printf("O valor do desconto e de %.2f\n", desconto);
		printf("O valor do salario a receber e de %.2f\n", sal_receber);	
	}
	if(salario > 2000){
		
		desconto = salario * 0.3;
		sal_receber = salario - desconto;
		
		printf("O valor do desconto e de %.2f\n", desconto);
		printf("O valor do salario a receber e de %.2f\n", sal_receber);
	}

	system("PAUSE");
	return 0; 
}



//**3. Dados o destino de um passageiro e se sua passagem será apenas de ida
ou de ida e volta, informar o preço se sua passagem conforme a tabela abaixo:**//

#include <stdio.h>
#include <stdlib.h>

int main(){
	
	int destino, passagem;
	
	printf("Informe o destino da viagem:\n ");
	printf("--------------------------\n");
	printf("1 - Regiao Norte\n");
	printf("2 - Regiao Nordeste\n");
	printf("3 - Regiao Centro-Oeste\n");
	printf("4 - Regiao Sul\n");
	printf("--------------------------\n");
	printf("Destino: ");
	scanf("%i", &destino);
	
	printf("Passagem 1 - Ida ou 2 - Ida/Volta: ");
	scanf("%i", &passagem);	
	
	if(destino == 1){
		if(passagem == 1){
			printf("O valor da passagem e de R$ 500.00\n");
		}
		else{
			printf("O valor da passagem e de R$ 900.00\n");
		}
	}
	else if(destino == 2){
		if(passagem == 1){
			printf("O valor da passagem e de R$ 350.00\n");
		}
		else{
			printf("O valor da passagem e de R$ 650.00\n");
		}
	}
	else if(destino == 3){
		if(passagem == 1){
			printf("O valor da passagem e de R$ 350.00\n");
		}
		else{
			printf("O valor da passagem e de R$ 600.00\n");
		}
	}
	else if(destino == 4){
		if(passagem == 1){
			printf("O valor da passagem e de R$ 300.00\n");
		}
		else{
			printf("O valor da passagem e de R$ 550.00\n");
		}
	}
	
	system("PAUSE");
	return 0;
}






//**4. As maçãs custam R$ 1,30 cada se forem compradas menos de uma dúzia, e
R$ 1,00 se forem compradas pelo menos 12. Escreva um programa que leia o
número de maçãs compradas, calcule e escreva o custo total da compra.**//

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(){
	
	int quant;
	float valor_compra;
	
	printf("Informe a quantidade de frutas compradas: ");
	scanf("%i", &quant);
	
	if(quant < 12){
		valor_compra = quant * 1.3;
		printf("O valor unitario e de R$ 1.30\n");
		printf("O valor total da compra e de R$ %.2f\n", valor_compra);
	}
	else{
		valor_compra = quant * 1.0;
		printf("O valor unitario e de R$ 1.00\n");
		printf("O valor total da compra e de R$ %2.f\n", valor_compra);
	}
	
	system("PAUSE");
	return 0;
}



//**5. Escreva um algoritmo que leia as idades de 2 homens e de 2 mulheres
(considere que as idades dos homens serão sempre diferentes entre si, bem
como as das mulheres). Calcule e escreva a soma das idades do homem maisvelho com a mulher mais nova, e o produto das idades do homem mais novo
com a mulher mais velha.**//


#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(){
	
	int idade1, idade2, idade3, idade4, soma, mult;
	
	printf("Digite a idade de uma pessoa do sexo masculino: ");
	scanf("%i", &idade1);
	printf("anos\n");
	printf("Digite a idade de outra pessoa do sexo masculino: ");
	scanf("%i", &idade2);
	printf("anos\n");
	printf("Digite a idade de uma pessoa do sexo feminino: ");
	scanf("%i", &idade3);
	printf("anos\n");
	printf("Digite a idade de outra pessoa do sexo feminino: ");
	scanf("%i", &idade4);
	printf("anos\n");
	
	if(idade1 > idade2 && idade3 > idade4){
		soma = idade1 + idade4;
		mult = idade2 * idade3;
		printf("A soma das idades do homem mais velho e da mulher mais nova e %i\n", soma);
		printf("O produto das idades do homem mais novo e da mulher mais velha e %i\n", mult);
	}
	else if(idade1 > idade2 && idade3 < idade4){
		soma = idade1 + idade3;
		mult = idade2 * idade4;
		printf("A soma das idades do homem mais velho e da mulher mais nova e %i\n", soma);
		printf("O produto das idades do homem mais novo e da mulher mais velha e %i\n", mult);
	}
	else if(idade1 < idade2 && idade3 > idade4){
		soma = idade2 + idade4;
		mult = idade1 * idade3;
		printf("A soma das idades do homem mais velho e da mulher mais nova e %i\n", soma);
		printf("O produto das idades do homem mais novo e da mulher mais velha e %i\n", mult);
	}
	else if(idade1 < idade2 && idade3 < idade4){
		soma = idade2 + idade3;
		mult = idade1 * idade4;
		printf("A soma das idades do homem mais velho e da mulher mais nova e %i\n", soma);
		printf("O produto das idades do homem mais novo e da mulher mais velha e %i\n", mult);
	}
	
	system("PAUSE");
	return 0;
}


//**6. Construa um programa que imprime a soma de todos os valores positivos
digitados pelo usuario ate que ele digite um número negativo.**//

#include <stdio.h>
#include <stdlib.h>

int main(void){

    int num=0,valor=0;
    do{

        printf("\n digite um numero:");
        scanf("%d",&num);
        if (num%2!=0){
        valor=valor+num;
        }
       } while(num%2!=0);
         printf("\n a soma dos numeros impares e %d:",valor);
}

//**7) Faça um programa que receba dois números X e Y, sendo X < Y. Calcule e
mostre:
(a) a soma dos números pares desse intervalo de números, incluindo os
números digitados;
(b) a multiplicação dos números ímpares desse intervalo, incluindo os
digitados;**//

int main()
{
    int num1,num2,cont,cont2,soma=0,produto=1;
    printf("informe 2 numeros,sendo o primeiro menor que o segundo:\n");
    system("pause");
    printf("\n\n");
    printf("digite o primeiro numero:");
    scanf("%d",&num1);
    printf("\n\n");
    printf("digite o segundo numero:");
    scanf("%d",&num2);
    cont=num1;
    cont2=num1;
     while(cont<=num2){
        if (cont%2==0){
            soma=soma+cont;
            }
            cont++;
                if(cont2%2!=0){
                    produto=produto*cont2;
                    }
                cont2++;
            }
             printf("\n\n a soma dos numeros pares e :%d",soma);
             printf("\n\n");
                    printf("\n a multiplicacao dos numeros impares e :%d",produto);
                    printf("\n\n");
    return 0;
    
    system("pause");
}


//**8. Escreva um programa que leia os dois lados de um quadrado e depois e
depois exiba esse quadrado a partir de asteriscos. Seu progrma deverá
funcionar para quadrados de todos os tamanhos. Por exemplo, se o prgrama
ler os lados 4 e 5 ele deverá exibir:**//
*****
*****
*****
*****

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(){
	
	float lado1, lado2, i, j;
	
	printf("Informe o tamnaho do primeiro lado do quadrado: ");
	scanf("%f", &lado1);
	printf("Informe o tamnaho do segundo lado do quadrado: ");
	scanf("%f", &lado2);
	
	for(i = 0; i < lado1; i++){
		for(j = 0; j < lado2; j++){
			printf("*");
		}
		printf("\n");
	}
	
	system("PAUSE");
	return 0;
}

//**9. Reescreva o programa do exercício 8 para que ele exiba um quadrado vazio
Por exemplo, se o programa ler os lados 4 e 5 ele deverá exibir:**//
*****
* *
* *
*****

#include <stdio.h>
#include <stdlib.h>

int main(){
    int i,j,c,d;
        printf("\n\n");
        for(i=0;i<5;i++){
            printf("*");
        }
            printf("\n\n");
            for(j=0;j<1;j++){
                printf("*   *");
            }
                printf("\n\n");
                 for(c=0;c<1;c++){
                    printf("*   *");
                }
                    printf("\n\n");
                         for(d=0;d<5;d++){
                            printf("*");
                        }
                                printf("\n\n");



    return 0;
}


//**10. MDC significa máximo divisor comum. O máximo divisor comum entre dois
ou mais números naturais é o maior de seus divisores. Dois números naturais
sempre tem divisores em comum. Como exemplo, o MDC de 16 e 24, MDC 16,
24 = 8, que é o maior número natural que divides ambos. Construir um
algoritmo em C para calcular o MDC de dois números naturais.**//


#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(){
	
	int num1, num2, resto;
	
	printf("Digite um numero: ");
	scanf("%i", &num1);
	printf("Digite um numero: ");
	scanf("%i", &num2);
	
	resto =num1%num2;
	
	while(resto != 0){
   	    num1    = num2;
		num2    = resto;
		resto = num1%num2;	
	}
	
	printf("O MDC desses numeros e %i\n", num2);
		
	system("PAUSE");
	return 0;
}
