# Ex16 Check for Balanced Parentheses Using Stack
## DATE:
## AIM:
To write a Java program that verifies whether the parentheses (brackets) in an input string are balanced — meaning each opening bracket (, {, [ has a corresponding and correctly ordered closing bracket ), }, ].

## Algorithm
1. Start the program.
2. Create a stack to store opening brackets.
3. Traverse each character in the input string.
4. If the character is an opening bracket, push it onto the stack.
5. If it is a closing bracket, check if the stack is empty or if it does not match the top element; if so, return unbalanced.
6. If it matches, pop the top element from the stack.
7. After processing all characters, if the stack is empty then the parentheses are balanced, otherwise they are not.
8. Stop the program. 

## Program:
```
/*
Program to verify whether the parentheses (brackets) in an input string are balanced
Developed by: Ramya.P
RegisterNumber:212223240137
*/
import java.util.*;

public class BalancedParentheses {
    public static boolean isBalanced(String str) {
        Stack<Character> stack = new Stack<>();

        for (char c : str.toCharArray()) {
            // Push opening brackets
            if (c == '(' || c == '{' || c == '[') {
                stack.push(c);
            }
            // Check closing brackets
            else if (c == ')' || c == '}' || c == ']') {
                if (stack.isEmpty()) {
                    return false;
                }
                char top = stack.pop();

                // Check for matching pairs
                if ((c == ')' && top != '(') ||
                    (c == '}' && top != '{') ||
                    (c == ']' && top != '[')) {
                    return false;
                }
            }
        }

        // If stack empty, it's balanced
        return stack.isEmpty();
    }

    public static void main(String[] args) {
        String input = "({[]})";

        if (isBalanced(input)) {
            System.out.println("Balanced Parentheses");
        } else {
            System.out.println("Not Balanced");
        }
    }
}

```

## Output:


<img width="384" height="184" alt="Screenshot 2025-11-15 220533" src="https://github.com/user-attachments/assets/ebf6021b-4ecf-4918-87b7-91d430c01830" />

## Result:
Thus,the program correctly checks whether an input string has balanced parentheses using a stack.
