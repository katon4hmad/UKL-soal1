# UKL-soal1
program untuk mencari bilangan prima
package latihanukl1;

import java.util.Scanner;

public class LatihanUKL1 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Masukkan bilangan: ");
        int n = input.nextInt();

        boolean prima = true;

        if (n <= 1) prima = false;
        else {
            for (int i = 2; i <= Math.sqrt(n); i++) {
                if (n % i == 0) {
                    prima = false;
                    break;
                }
            }
        }

        if (prima)
            System.out.println(n + " adalah bilangan prima.");
        else
            System.out.println(n + " bukan bilangan prima.");
    }
}
