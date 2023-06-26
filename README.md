# VasjaTask
import java.util.Scanner;
public class VasjaTask1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Василий, введите значение x: ");
        int x = scanner.nextInt();
        int rows = x;
        int columns = x;
        int[][] array = new int[rows][columns];

        for(int n = 0; n < rows*columns; n++) {
            int i = n / columns;
            int j = i % 2 == 0 ? n % columns : columns - 1 - n % columns;
            array[i][j] = n;
        }
        print2DArray(array);
    }
    public static void print2DArray(int[][] values) {
        for (int i = 0; i < values.length; i++) {
            for (int j = 0; j < values[i].length; j++) {
                System.out.print(values[i][j]+" ");
            }
            System.out.println();
        }
    }

}
