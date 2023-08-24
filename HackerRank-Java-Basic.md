# HackerRank-Java-Basic
HackerRank Java Basic Certification Test Solution
- The Adder Class
- Multi Sum

## The Adder Class
```yaml
import java.util.Scanner;

abstract class Calculator {
    abstract int add(int a, int b);
}
/*
 Write the Adder class here. Do not use an access modifier at the beginning of your class declaration.
 */
 class Adder extends Calculator{
     @Override
     int add(int a, int b) {
         // TODO Auto-generated method stub
         return a + b;
     }
 }
public class Solution {
    public static void main(String[] args) {
        int a, b;
        try (Scanner scan = new Scanner(System.in)) {
            a = scan.nextInt();
            b = scan.nextInt();
        }

        Calculator adderObject = new Adder();
        System.out.println("The sum is: " + adderObject.add(a, b));
    }
}
```

## Multi Sum
```yaml
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

class Arithmetic{
    public int sum(Integer[] array) {
        int total = 0;
        for (int i = 0; i < array.length; i++) {
            total = total + array[i];
        }
        return total;
    }
    public String sum(String[] array) {
        String sum = "";
        for (int n = 0; n < array.length; n++){
            sum = sum.concat(array[n]);   
        }
        return sum;
    }
}

public class Solution {
    public static void main(String args[] ) throws Exception {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT */
        Arithmetic arithmetic = new Arithmetic();
        Scanner sc = new Scanner(System.in);
        String line = sc.nextLine();
        String[] values = line.split(" ");

        try{
            Integer.parseInt(values[0]);
            
            Integer[] ia = new Integer[values.length];
            for(int i = 0; i < values.length; i++){
                ia[i] = new Integer(values[i]);
            }
            System.out.println(arithmetic.sum(ia));
        }catch(NumberFormatException nfe){
            System.out.println(arithmetic.sum(values));
        }
    }
}
```
