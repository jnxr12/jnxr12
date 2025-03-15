import java.util.Scanner;

public class main {
    public static void main(String[] args) {
        Scanner Scanner = new Scanner(System.in);

        System.out.print("Enter a number from 1 - 7 representing a day of the week: ");
        int day = Scanner.nextInt();

        if (day < 1 || day > 7) {
            System.out.println("EROR Please enter a number between 1 and 7.");
        } else {

            String kind = (day == 1 || day == 7) ? "weekend" : "weekday";


            boolean Prime = Prime(day);
            System.out.println("Is the day a prime number? " + Prime);


            String evenodd = (day % 2 == 0) ? "even" : "odd";
            System.out.println("The day is " + evenodd + " ");
        }

        Scanner.close();



    }


    public static boolean Prime(int num) {
        if (num < 2) return false;
        for (int i = 2; i * i <= num; i++) {
            if (num % i == 0) return false;
        }
        return true;
    }
}
