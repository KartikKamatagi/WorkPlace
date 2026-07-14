import java.util.Scanner;

public class NumberPrograms {

    // 1. Reverse a Number
    public static int reverseNumber(int num) {
        int rev = 0;
        while (num > 0) {
            rev = rev * 10 + (num % 10);
            num /= 10;
        }
        return rev;
    }

    // 2. Palindrome Number
    public static boolean isPalindrome(int num) {
        return num == reverseNumber(num);
    }

    // 3. Count Digits
    public static int countDigits(int num) {
        if (num == 0) return 1;
        int count = 0;
        while (num > 0) {
            count++;
            num /= 10;
        }
        return count;
    }

    // 4. Sum of Digits
    public static int sumOfDigits(int num) {
        int sum = 0;
        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        return sum;
    }

    // 5. Armstrong Number
    public static boolean isArmstrong(int num) {
        int original = num;
        int digits = countDigits(num);
        int sum = 0;
        while (num > 0) {
            int lastDigit = num % 10;
            sum += Math.pow(lastDigit, digits);
            num /= 10;
        }
        return sum == original;
    }

    // 6. Prime Number
    public static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) return false;
        }
        return true;
    }

    // Helper for Factorial
    public static int factorial(int n) {
        int fact = 1;
        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }

    // 7. Fibonacci Series (Prints first n terms)
    public static void printFibonacci(int terms) {
        int a = 0, b = 1;
        for (int i = 0; i < terms; i++) {
            System.out.print(a + " ");
            int next = a + b;
            a = b;
            b = next;
        }
        System.out.println();
    }

    // 9. GCD & LCM
    public static int getGCD(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }

    public static int getLCM(int a, int b) {
        return (a * b) / getGCD(a, b);
    }

    // 10. Perfect Number
    public static boolean isPerfect(int num) {
        int sum = 0;
        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) sum += i;
        }
        return sum == num;
    }

    // 10. Strong Number / Peterson Number
    public static boolean isStrongOrPeterson(int num) {
        int original = num;
        int sum = 0;
        while (num > 0) {
            sum += factorial(num % 10);
            num /= 10;
        }
        return sum == original;
    }

    // 10. Neon Number
    public static boolean isNeon(int num) {
        int square = num * num;
        return sumOfDigits(square) == num;
    }

    // 10. Spy Number
    public static boolean isSpy(int num) {
        int sum = 0, product = 1;
        while (num > 0) {
            int digit = num % 10;
            sum += digit;
            product *= digit;
            num /= 10;
        }
        return sum == product;
    }

    // 10. Duck Number
    public static boolean isDuck(String numStr) {
        // Must not start with '0' but must contain '0'
        if (numStr.charAt(0) == '0') return false;
        return numStr.contains("0");
    }

    
    }
}
