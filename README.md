# Lista 04
## Introdução ao Java
>Depois que coloquei em pratica a lógica de programação no portugol, agora fiz os seguintes exercícios no Java:
- **Validador de Maioridade:** Objetivo era criar um programa para ler a idade do usúario, se for maior de 18 o programa indica acesso liberado se não acesso negado.
- **O Radar de Velocidade:** O objetivo era criar um programa para ler a velocidade de carro e se passasse de 80 km é para cobrar 7 reais por KM ultrapassado, se não passar dos 80 km o programa indica Boa Viagem!.
- **Sistema de Aprovação Escolar:** O objetivo era criar um programa que faz a leitura de duas notas e calcula a média no final.
- **Par ou Ímpar:** O objetivo era criar um programa que faz a leitura de um número e informa para o usúario se é par ou ìmpar.
- **Analisador de Triângulos:** O objetivo era criar um programa que faz a leitura de três valores (lados de um triângulo). Primeiro, verifique se eles podem formar um triângulo (a soma de dois lados deve ser sempre maior que o terceiro). Se sim, classifique em: - Equilátero: Todos os lados iguais. - Isósceles: Dois lados iguais. - Escaleno: Todos os lados diferentes.

>Para a resolução dessas atividades usei a estrutura `if/else` no java

---

## Programa
### Validador de Maioridade:
```Java
import java.util.Scanner;

public class Validadordeidade{
public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    
    int idade;

    System.out.println("Digite sua idade");
    idade=sc.nextInt();

    if(idade>=18){
        System.out.println("Acesso Permitido");
}else{
    System.out.println("Acesso negado");
}


}
}
```
---
### O Radar de Velocidade:
```Java
import java.util.Scanner;
public class Radar {

public static void main(String[] args){
Scanner sc = new Scanner(System.in);
int velocidade;
int limite=80;
int multa;
System.out.println("Qual a velocidade do veiculo?:");
velocidade = sc.nextInt();
if(velocidade>limite){
    multa=(velocidade-limite) * 7;
    System.out.println("O valor da multa que deve ser paga é de:" + multa +"$");
    
}else{
    System.out.println("Boa viagem!");
}
 }

 }
```
---

### Sistema de Aprovação Escolar:
```Java
import java.util.Scanner;
public class aprovacaoescolar{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double nota1;
        double nota2;
        double media;
        System.out.println("Digite uma nota:");
        nota1 = sc.nextDouble();
           System.out.println("Digite outra nota:");
           nota2 = sc.nextDouble();
          media=(nota1+nota2)/2;
              System.out.println("A média do aluno foi:" + media);


    }
}
```
---
### Par ou Ímpar:
```Java
import java.util.Scanner;
public class parouimpar{
    public static void main(String[] args){
        Scanner sc= new Scanner(System.in);
        int num;
         System.out.println("Digite um numero:");
         num=sc.nextInt();
         if(num %2==0){
         System.out.println("Par");
         }else{
            System.out.println("Impar");
         }
    
 }
}

```
---
### Analisador de Triângulos:

```Java
import java.util.Scanner;

public class triangulos{                                                            
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

      
        System.out.println("Digite o primeiro lado do triangulo:");
        double a = sc.nextDouble();

        System.out.println("Digite o segundo lado do triangulo:");
        double b = sc.nextDouble();

        System.out.println("Digite o terceiro lado do triangulo:");
        double c = sc.nextDouble();

        if (a + b > c && a + c > b && b + c > a) {
            // Classificação
            if (a == b && b == c) {
                System.out.println("Triangulo Equilatero");
            } else if (a == b || b == c || a == c) {
                System.out.println("Triângulo Isosceles");
            } else {
                System.out.println("Triangulo Escaleno");
            }
        } else {
            System.out.println("Os valores nao formam um triangulo");
        }

        sc.close();
    }
}
```
---


