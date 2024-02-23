# verificaisograma


package VerificaIsograma;


import java.util.Scanner;

public class VerificaIsograma {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita ao usuário que insira a palavra
        System.out.println("Digite uma palavra:");
        String palavra = scanner.nextLine().toLowerCase();

        // Verifica se a palavra é um isograma
        boolean ehIsograma = true;
        for (int i = 0; i < palavra.length(); i++) {
            char letra = palavra.charAt(i);
            if (Character.isLetter(letra) && palavra.indexOf(letra, i + 1) != -1) {
                ehIsograma = false;
                break;
            }
        }

        // Exibe o resultado
        if (ehIsograma) {
            System.out.println("A palavra é um isograma.");
        } else {
            System.out.println("A palavra não é um isograma.");
        }

        // Fecha o scanner
        scanner.close();
    }
}
