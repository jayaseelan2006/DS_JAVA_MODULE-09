# Ex17 Reversing a String Using Stack Data Structure
## DATE:
## AIM:
To write a Java program that reverses an input string using a stack, without using built-in reverse functions.

## Algorithm
1. Start the program.
2. Create an empty stack to store characters.
3. Read the input string from the user.
4. Push each character of the string onto the stack.
5. Pop characters from the stack one by one and append them to a new string (reversed string).
6. Print the reversed string.
7. Stop the program   

## Program:
```
/*
Program to reverses an input string using a stack

*/

import java.util.Stack;
import java.util.Scanner;

public class ReverseStringStack {
    public static void main(String[] args) {
        Stack<Character> stack = new Stack<>();
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String input = sc.nextLine();

        for (char ch : input.toCharArray()) {
            stack.push(ch);
        }

        String reversed = "";
        while (!stack.isEmpty()) {
            reversed += stack.pop();
        }

        System.out.println("Reversed String: " + reversed);
    }
}

```

## Output:

<img width="359" height="191" alt="Screenshot 2025-11-16 072814" src="https://github.com/user-attachments/assets/cdaaf2ad-bcb1-4160-87fe-8318229334ed" />


## Result:
Thus, the program successfully reverses the given string using a stack without relying on built-in reverse functions.
