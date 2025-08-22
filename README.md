# MediaAlunoJava
Montei esse código com a intenção do usuário poder digitar quantas notas ele quer digitar e quais seus respectivos valores. Após as notas digitadas, o Java imprimirá no console a média total das notas.

```java
package arrays;

import java.util.Scanner;

public class Desafio {
	
	public static void main(String[] args) {
		Scanner entrada = new Scanner(System.in);
		System.out.print("Quantas notas você quer digitar? ");
		int quantNotas = entrada.nextInt();	
		entrada.nextLine();
		
		double[] notasAluno = new double[quantNotas];
		
		
		for(int i = 0; i < notasAluno.length; i++) {
			System.out.print("Digite a nota: ");
			notasAluno[i] = entrada.nextDouble();
			entrada.nextLine();
		}
		
		double totalNotas = 0;
		
		for(double nota: notasAluno){
			totalNotas += nota;
		}
		
		double mediaAluno = totalNotas / notasAluno.length;
		
		System.out.printf("Média: %.2f" ,mediaAluno );
		entrada.close();
	}
}
```
