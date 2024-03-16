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
