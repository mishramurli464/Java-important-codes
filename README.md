# Java-important-codes  
## check if a given string is a palindrome  

```java
/*package whatever //do not write package name here */

import java.io.*;
import java.util.Scanner;

class strpal {
	public static void main (String[] args) {
		String name;
		int i;
		int j=0;
		Scanner sc= new Scanner(System.in);
		System.out.println("enter the name");
		name=sc.nextLine();
		int l =name.length();
		for(i=0;i<=l/2-1;i++)
		{
		    if (name.charAt(i)==name.charAt(l-i-1))
		    {
		        j=j+1;
		    }
		     else
		      {
		         break;
		      }
		}
	
	 if (j==l/2)  
	 {
	  System.out.println("palindrom");
	 }
	 else
	 {
	  System.out.println(" not palindrom");
	 }
	    
	}
	
}
```
## Check if two strings are anagrams  
```java
import java.io.*;
import java.util.Scanner;
import java.util.Arrays;
class strpal {
	public static void main (String[] args) {
	    String s1;
	    String s2;
	    Scanner sc= new Scanner(System.in);
	    s1 = sc.nextLine();
	    s2 = sc.nextLine();
	    char[] char1 =s1.toCharArray();
	    char[] char2 =s2.toCharArray();
	    int l1= char1.length;
	    int l2= char2.length;
	    if(l1!=l2)
	    {
	     System.out.println("not anagram");  
	     System.exit(0);
	    }
	    Arrays.sort(char1);
	    Arrays.sort(char2);
	    int i;
	    
	    for(i=0;i<l1;i++)
	    if (char1[i]==char2[i])
	    {
	        
	    }
	    else
	    {
	        System.out.println("not palindrome");  
	        System.exit(0);
	    }
	    
	    System.out.println("is palindrome");
	
	
	}
```

## to count the occurance of a particular character in the give string  
```java
/*package whatever //do not write package name here */

import java.io.*;
import java.util.Scanner;
import java.util.Arrays;
class strpal {
	public static void main (String[] args) {
	    Scanner sc= new Scanner(System.in);
	    String s1= sc.nextLine();
	    // char[] charArray = s1.toCharArray();
	    char c1=sc.next().charAt(0);
	    int l=s1.length();
	    int i;
	    int count=0;
	    for(i=0;i<l;i++)
	    {
	        
	        if(s1.charAt(i)==c1)
	        {
	            count+=1;
	        }
	    }
	    
	    System.out.println("ocuurance:"+ count);
	
	
	}
	
}
```
## to find matching characters between two strings s1 and s2. 
```java
import java.util.Scanner;
import java.io.*;

class abc {
    public static void main( String[] args)
    {
        
        String s1;
        String s2;
        Scanner sc= new Scanner(System.in);
        s1=sc.nextLine();
        s2=sc.nextLine();
        int l1 = s1.length();
        int l2 = s2.length();
        for(int i=0; i<l1; i++)
        {
        for(int j=0; j<l2; j++)
        {
         if (s1.charAt(i)==s2.charAt(j) ) 
         {
         if (i==0 || s1.charAt(i)!=s2.charAt(i-1))
         {
         System.out.println("matching character" + " " + s1.charAt(i));
         break;
         }
         }
        }
        }
        
    }
}

```
 ## to count the occurrences of each character in the input string s1
```java
import java.util.Scanner;

class strpal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String s1 = sc.nextLine();
        int l = s1.length();
        int i, j;
        
        for (i = 0; i < l; i++) {
            int count = 0; // Reset count for each character
            
            for (j = 0; j < l; j++) {
                if (s1.charAt(i) == s1.charAt(j)) {
                    count++;
                }
            }
            
            // Print the character along with its count, but only once per character
            if (i == 0 || s1.charAt(i) != s1.charAt(i - 1)) {
                System.out.println(s1.charAt(i) + " - " + count);
            }
        }
    }
}
```
## to count vovels and consonant in string

```java
import java.util.Scanner;  
class consvow{
    public static void  main (String[] args)
    {
        Scanner sc= new Scanner(System.in);
        String s = sc.nextLine();
        int i;
        int count =0;
        int l = s.length();
        
        for (i=0;i<l;i++) 
        {
            if (s.charAt(i)== 'a' || s.charAt(i)== 'e' || s.charAt(i)== 'i' || s.charAt(i)== 'o' || s.charAt(i)== 'u')
            {
                count+=1;
            }
        }
        System.out.println("vowels:" + count);
        int cons= l - count;
        System.out.println("consonants:" + cons);
    }
    
}
```

## finding and printing matching elements in an array.  
```java
import java.util.Scanner;

class consvow {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the size of the array:");
        int size = sc.nextInt();
        int[] arr = new int[size];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            arr[i] = sc.nextInt();
        }

        for (int i = 0; i < size; i++) {
            for (int j = i+1; j<size; j++) {
                if (arr[i] == arr[j]) {
                    if (i==0 || arr[i] != arr[i-1] ){
                    System.out.println("matching element-" + arr[i]);
                    }
                    break; // Exit the inner loop once a matching element is found
                }
            }
        }
        
    }
}

```

## to implement a method to reverse an array

```java
import java.util.Scanner;

class consvow {
    
    public static void rev(int[] arr, int size)
    {
        int i=0;
        int j= size -1;
        int temp=0;
        while(i<j)
        {
            temp = arr[i];
            arr[i]=arr[j];
            arr[j]=temp;
            i++;
            j--;
        }
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the size of the array:");
        int size = sc.nextInt();
        int[] arr = new int[size];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            arr[i] = sc.nextInt();
        }

     
       rev(arr, size);
       for (int i = 0; i < size; i++)
       {
        System.out.println(arr[i]);
       }
       
    }
}
```
## printing fibbonaci series  
```java
import java.util.Scanner;

class consvow {
    public static void main(String[] args) {
        int a=0;
        int b=1;
        int c,i;
        int term;
        Scanner sc = new Scanner(System.in);
        term = sc.nextInt();
        for (i=0;i<term;i++)
        {
            System.out.println(a + "");
            c=a+b;
            a=b;
            b=c;
        }
    }
}

```
##  printing fibbonaci series  using recursion
```java
import java.util.Scanner;

public class Fibonacci {
    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        } else {
            return fibonacci(n - 1) + fibonacci(n - 2);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of Fibonacci numbers to generate:");
        int count = sc.nextInt();
        System.out.println("Fibonacci Series:");
        for (int i = 0; i < count; i++) {
            System.out.print(fibonacci(i) + " ");
        }
    }
}
```

## printing fibbonaci series  using recursion( by creating instance)
```java
import java.util.Scanner;

class  fibonacci{
    int fib(int n)
    {
        if (n<=1)
        {
            return n;
        }
        else
        {
            return (fib(n-1) + fib(n-2));
        }
        
    }
    public static void main(String[] args) {
       int i;
       fibonacci f1 = new fibonacci();
       Scanner sc = new Scanner(System.in);
       int temp = sc.nextInt();
       for (i=0;i<temp ;i++ ) 
       {
        System.out.println(f1.fib(i) + " " );    
       }
        }
    }

```

## Java code to find the average of numbers in a list:  

```java
import java.util.*;
class avg{
    
    public static void main(String args[])
    {
        ArrayList<Integer> list = new ArrayList<>();
        int num;
        Scanner sc= new Scanner(System.in);
        num = sc.nextInt();
        System.out.println("enter the numbers(enter -1 to exit)");
        while(num!= -1)
        {
            list.add(num);
            num = sc.nextInt();
        }
        int sum=0;
        for(int number: list)
        {
            sum+=number;
        }
        int s = list.size();
        
        double avg = sum/s;
        System.out.println("average :" +avg);
    }
}
```
