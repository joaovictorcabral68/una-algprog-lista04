# Lista 02 - Java
## Introdução ao Java
>Depois que coloquei em pratica a lógica de programação no portugol, agora fiz os seguintes exercícios no Java:
- **Mensagem de número:** Solicita um número e o exibe no console
- **Operações basicas:** Pede dois números e mostra a soma, subtração e multiplicação.
- **Média bimestral:** Calcula a média a partir de 4 notas informadas.
- **Cálculo combustivel:** Calcula o valor total pago com base no preço do litro e quantidade vendida.
- **Eurotrip:** Calcula o custo total de uma viagem para três destinos (Alemanha, Portugal e Itália) considerando o preço por destino e a quantidade de pessoas.

>Para a resolução dessas atividades usei a estrutura `if/else` no java

---

## Programa
### Mensagem de número:
```Java
import java.util.Scanner;

public class Exercicio1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite um número: ");
        int number = scanner.nextInt();

        System.out.println("Número digito foi: " + number);

        scanner.close();
    }
}
```
---
### Operações basicas:
```Java
import java.util.Scanner;

public class Exercicio2 {
    public static void main(String[] args) {

        
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite um número: ");
        int number1 = scanner.nextInt();

        System.out.println("Digite outro número: ");
        int number2 = scanner.nextInt();

        System.out.println("Soma: " + (number1 + number2));
        System.out.println("Divisão: " + (number1 - number2));
        System.out.println("Multiplicação: " + (number1 / number2));


        scanner.close();

    }
}
```
---

### Média bimestral:
```Java
import java.util.Scanner;

public class Exercicio3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double media;

        System.out.println("Digite sua nota do 1º bimestre: ");
        double nota1 = scanner.nextDouble();

        System.out.println("Digite sua nota do 2º bimestre: ");
        double nota2 = scanner.nextDouble();

        System.out.println("Digite sua nota do 3º bimestre: ");
        double nota3 = scanner.nextDouble();

        System.out.println("Digite sua nota do 4º bimestre: ");
        double nota4 = scanner.nextDouble();

        media = ((nota1 + nota2 + nota3 + nota4) / 4);
        
        System.out.println("A média das suas notas é: " + media);

        scanner.close();
    }
}
```
---
### Cálculo combustivel:
```Java
import java.util.Scanner;

public class Exercicio4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double precoGasolina;
        double litrosComprados;
        double valorTotal;

        System.out.println("Digite o preço da gasolina: ");
        precoGasolina = scanner.nextDouble();
        
        System.out.println("Digite o números de litros: ");
        litrosComprados = scanner.nextDouble();
        
        valorTotal = precoGasolina * litrosComprados;
        System.out.println("Valor total: R$" + valorTotal);

        scanner.close();
    }
}
```
---
### Eurotrip:

```Java
import java.util.Scanner;

public class Exercicio5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int qtdPessoasAlemanha;
        double precoAlemanha;

        int qtdPessoasPortugal;
        double precoPortugal;

        int qtdPessoasItalia;
        double precoItalia;

        System.out.println("Digite o valor da viagem para Alemanha: ");
        precoAlemanha = scanner.nextDouble();

        System.out.println("Digite a quantidade de pessoas que vão para a viagem para Alemanha: ");
        qtdPessoasAlemanha = scanner.nextInt();

        System.out.println("Digite o valor da viagem para Portugal: ");
        precoPortugal = scanner.nextDouble();

        System.out.println("Digite a quantidade de pessoas que vão para a viagem para Portugal: ");
        qtdPessoasPortugal = scanner.nextInt();

        System.out.println("Digite o valor da viagem para Italia: ");
        precoItalia = scanner.nextDouble();

        System.out.println("Digite a quantidade de pessoas que vão para a viagem para Italia: ");
        qtdPessoasItalia = scanner.nextInt();

        System.out.println("Valor total (Viagem Alemanha): R$" + (qtdPessoasAlemanha * precoAlemanha));
        System.out.println("Valor total (Viagem Portugal): R$" + (qtdPessoasPortugal * precoPortugal));
        System.out.println("Valor total (Viagem Italia): R$" + (qtdPessoasItalia * precoItalia));
        System.out.println("Valor total (Eurotrip): R$" + ((qtdPessoasAlemanha * precoAlemanha) + (qtdPessoasPortugal * precoPortugal) + ((qtdPessoasItalia * precoItalia))));

        scanner.close();
    }
}
```
---


