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
