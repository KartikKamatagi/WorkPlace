1. Reverse a Number
Java
public class ReverseNumber {
    public static void main(String[] args) {
        int num = 1234, rev = 0;
        while (num > 0) {
            rev = rev * 10 + (num % 10);
            num /= 10;
        }
        System.out.println("Reversed Number: " + rev);
    }
}

2. Palindrome Number
Java
public class PalindromeNumber {
    public static void main(String[] args) {
        int num = 121, original = num, rev = 0;
        while (num > 0) {
            rev = rev * 10 + (num % 10);
            num /= 10;
        }
        if (original == rev) {
            System.out.println(original + " is a Palindrome.");
        } else {
            System.out.println(original + " is not a Palindrome.");
        }
    }
}

3. Count Digits
Java
public class CountDigits {
    public static void main(String[] args) {
        int num = 98765, count = 0;
        while (num > 0) {
            count++;
            num /= 10;
        }
        System.out.println("Total Digits: " + count);
    }
}
4. Sum of Digits
Java
public class SumOfDigits {
    public static void main(String[] args) {
        int num = 543, sum = 0;
        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        System.out.println("Sum of Digits: " + sum);
    }
}

5. Armstrong Number
Java
public class ArmstrongNumber {
    public static void main(String[] args) {
        int num = 153, original = num, temp = num;
        int digits = 0, sum = 0;
        
        while (temp > 0) { digits++; temp /= 10; } // Count digits
        
        temp = num;
        while (temp > 0) {
            int lastDigit = temp % 10;
            sum += Math.pow(lastDigit, digits);
            temp /= 10;
        }
        System.out.println(original + (sum == original ? " is an Armstrong number." : " is not an Armstrong number."));
    }
}
6. Prime Number
Java
public class PrimeNumber {
    public static void main(String[] args) {
        int num = 29;
        boolean isPrime = num > 1;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        System.out.println(num + (isPrime ? " is a Prime number." : " is not a Prime number."));
    }
}
7. Fibonacci Series
Java
public class Fibonacci {
    public static void main(String[] args) {
        int terms = 8, a = 0, b = 1;
        System.out.print("Fibonacci Series: ");
        for (int i = 0; i < terms; i++) {
            System.out.print(a + " ");
            int next = a + b;
            a = b;
            b = next;
        }
    }
}
8. Factorial
Java
public class Factorial {
    public static void main(String[] args) {
        int num = 5, fact = 1;
        for (int i = 1; i <= num; i++) {
            fact *= i;
        }
        System.out.println("Factorial of " + num + " is: " + fact);
    }
}
9. GCD & LCM
Java
public class GcdLcm {
    public static void main(String[] args) {
        int n1 = 12, n2 = 18;
        int a = n1, b = n2;
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        int gcd = a;
        int lcm = (n1 * n2) / gcd;
        System.out.println("GCD: " + gcd + ", LCM: " + lcm);
    }
}
10. Special Numbers
Perfect Number
Java
public class PerfectNumber {
    public static void main(String[] args) {
        int num = 6, sum = 0;
        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) sum += i;
        }
        System.out.println(num + (sum == num ? " is a Perfect Number." : " is not a Perfect Number."));
    }
}
