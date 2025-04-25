## allprime
# Question:
Write a Java program to find and print all prime numbers between 1 and a given number n using the Sieve of Eratosthenes algorithm.
# Algorithm:
1.Input: Read an integer n from the user.

2. Create: A boolean array isPrime[0..n] and initialize all elements to true (except index 0 and 1).

3.Sieve Logic:

4. Start from 2 up to √n.

5. For each prime number p, mark its multiples as false.

6. Print: All numbers marked as true are prime.
# JaVA Program:
```
import java.util.Scanner;

public class allprime
{
    public static void main(String[] args) {
        Scanner ip =  new Scanner(System.in);
    int r = ip.nextInt();
    boolean[] isPrime = new boolean[r+1];
    for(int i=2;i<r;i++)
    {
    isPrime[i] =true;
    }

    for(int j = 2; j*j < r;j++)
    {
        if(isPrime[j])
        {
            for (int k = j * j; k <= r; k += j) { 
                isPrime[k] = false;
            }
        }
    }
    for (int i = 2; i <= r; i++) {
        if (isPrime[i]) {
            System.out.print(i + " ");
        }
    }
    
   
    
    ip.close();
    
    }
}
// to find all the prime number till the range 1 to n
```
# output:
![image](https://github.com/user-attachments/assets/78958f8c-7142-4b53-b174-c7e517fc32dd)
# result:
The program successfully takes an upper limit from the user and prints all prime numbers between 1 and n using the Sieve of Eratosthenes method.
