# Ex19 Palindrome Check Using Deque
## DATE: 22/11/2025
## AIM:
To design a program that checks whether a given message is a palindrome by removing all non-alphanumeric characters, converting all characters to lowercase, and using a deque data structure for comparison.


## Algorithm
1. Start the program.
2. Read an input string from the user.
3. Remove all non-alphanumeric characters from the string.
4. Convert all characters to lowercase for uniform comparison.
5. Create a deque (double-ended queue).
6. Insert each character of the cleaned string into the deque.
7. While the deque has more than one element:
   - Remove one character from the front and one from the rear.
   - Compare both characters.
   - If they are not equal, the string is not a palindrome.
8. If all pairs match, the string is a palindrome.
9. Display the result.

## Program:
```java
/*
Program to checks whether a given message is a palindrome by removing all non-alphanumeric characters.
Developed by: Vinnush kumar L S
Register Number: 212223230244
*/

import java.util.*;

public class PalindromeChecker {
    
    public static boolean isPalindrome(String message) {
        // Convert to lowercase and remove non-alphanumeric characters
        message = message.toLowerCase().replaceAll("[^a-z0-9]", "");
        
        Deque<Character> deque = new ArrayDeque<>();
        
        // Add all characters to the deque
        for (char c : message.toCharArray()) {
            deque.addLast(c);
        }
        
        // Compare characters from both ends
        while (deque.size() > 1) {
            if (deque.pollFirst() != deque.pollLast()) {
                return false;  // Mismatch found
            }
        }
        
        return true;  // All characters matched
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        //System.out.println("Enter a message:");
        String input = scanner.nextLine();

        if (isPalindrome(input)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a palindrome");
        }

        scanner.close();
    }
}

```

## Output:
<img width="378" height="128" alt="image" src="https://github.com/user-attachments/assets/8b524458-975d-45cb-bb5a-68490347aee3" />

## Result:
The program successfully removes all non-alphanumeric characters, converts the text to lowercase, and uses a deque to efficiently compare characters from both ends. Hence, it determines whether the string is a palindrome.
