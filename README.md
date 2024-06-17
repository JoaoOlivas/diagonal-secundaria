import java.util.Scanner;

public class MenorElementoDiagonalSecundaria {

    public static void main(String[] args) {
    
        int[][] matriz = lerMatriz();
        
        int menorElementoDiagonalSecundaria = encontrarMenorElementoDiagonalSecundaria(matriz);
        
        System.out.println("Menor elemento da diagonal secundária: " + menorElementoDiagonalSecundaria);
        
    }

    
    public static int[][] lerMatriz() {
    
        Scanner scanner = new Scanner(System.in);
        
        int[][] matriz = new int[6][6];

        System.out.println("Digite os elementos da matriz A(6,6):");
        
        for (int i = 0; i < 6; i++) {
        
            for (int j = 0; j < 6; j++) {
            
                matriz[i][j] = scanner.nextInt();
                
            }
            
        }

        return matriz;
        
    }

    
    public static int encontrarMenorElementoDiagonalSecundaria(int[][] matriz) {
    
        int menor = matriz[0][5]; 

        for (int i = 1; i < 6; i++) {
        
            int elementoDiagonalSecundaria = matriz[i][5 - i];
            
            if (elementoDiagonalSecundaria < menor) {
            
                menor = elementoDiagonalSecundaria;
                
            }
            
        }

        return menor;
        
    }
}
