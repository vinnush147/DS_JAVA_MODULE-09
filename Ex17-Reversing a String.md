# Ex17 Reversing a String Using Stack Data Structure
## DATE: 22/11/25
## AIM:
To write a Java program that reverses an input string using a stack, without using built-in reverse functions.

## Algorithm
1. Start the program.
2. Read the input string from the user.
3. Create an empty stack of characters.
4. Traverse the string and push each character onto the stack.
5. Pop each character from the stack and append it to a new string — this gives the reversed string.
6. Display the reversed string.
7. Stop the program.

## Program:
```java
/*
Program to reverses an input string using a stack
Developed by: Vinnush kumar L S
Register Number: 212223230244
*/

import java.util.Scanner;
import java.util.Stack;

public class ReverseStringWithStack {

    public static String reverseString(String input) {
         Stack<Character> stack=new Stack<>();
        for(char ch:input.toCharArray())
        {
            stack.push(ch);
        }
        StringBuilder rev=new StringBuilder();
        while(!stack.isEmpty())
        {
            rev.append(stack.pop());
        }
        return rev.toString();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String reversed = reverseString(input);
        System.out.println(reversed);

        scanner.close();
    }
}

```

## Output:
<img width="407" height="144" alt="image" src="https://github.com/user-attachments/assets/339f5baa-d8ed-4d30-aa79-9630ca797ff6" />

## Result:
Thus, the program successfully reverses the given string using a stack without relying on built-in reverse functions.
