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

class strpal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String s1 = sc.nextLine();
        String s2 = sc.nextLine();
        int l1 = s1.length();
        int l2 = s2.length();
        
        for (int i = 0; i < l1; i++) {
            boolean foundMatch = false; // Flag to track if a match is found for the current character in s1
            for (int j = 0; j < l2; j++) {
                if (s1.charAt(i) == s2.charAt(j)) {
                    System.out.println("Matching: " + s1.charAt(i));
                    foundMatch = true;
                    break; // Exit inner loop once a match is found
                }
            }
            if (!foundMatch) {
                System.out.println("Not Matching: " + s1.charAt(i));
            }
        }
    }
}

```
