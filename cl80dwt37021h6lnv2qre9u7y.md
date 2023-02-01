# CodeChef Problem Code: CREDSCORE solution in java.

**Solution**

*Problem Code:* **CREDSCORE**

*Contest Code:* [**LTIME106**](https://www.codechef.com/LTIME106)

Difficulty Rating: **459**



### Problem

To access CRED programs, one needs to have a credit score of **750** or more.
Given that the present credit score is **X**, determine if one can access CRED programs or not.

If it is possible to access CRED programs, output **YES**, otherwise output **NO**.


### Input Format

The first and only line of input contains a single integer **X**, the credit score.

### Output Format

Print **YES** if it is possible to access CRED programs. Otherwise, print **NO**.

You may print each character of the string in uppercase or lowercase (for example, the strings **YeS**, **yEs,** **yes**, and **YES** will all be treated as identical).

### Constraints

> -    0 ≤ X≤1000


### Subtasks

*   **Subtask 1 (100 points):** Original constraints.

### Sample 1:

Input

Output

823

YES

### Explanation:

Since 823≥750, it is possible to access CRED programs.

### Sample 2:

Input

251

Output

NO

### Explanation:

Since 251<750, it is not possible to access CRED programs.

### Solution:

```
/\* package codechef; // don't place package name! \*/

import java.util.\*;  
import java.lang.\*;  
import java.io.\*;

/\* Name of the class has to be "Main" only if the class is public. \*/  
class Codechef  
{  
 public static void main (String\[\] args) throws java.lang.Exception  
 {  
  // your code goes here  
  Scanner sc = new Scanner(System.in);  
  int x = sc.nextInt();  
  if(x>=750){  
      System.out.println("YES");  
  }  
  else{  
      System.out.println("NO");  
  }  
    
 }  
}
```