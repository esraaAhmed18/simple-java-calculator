# 🧮 Simple Java Calculator

A simple, user-friendly command-line calculator built using **Java**. This application allows users to perform basic arithmetic operations interactively through a console interface.

---

## ✨ Features

- ➕ **Addition** (`+`)
- ➖ **Subtraction** (`-`)
- ✖️ **Multiplication** (`*`)
- ➗ **Division** (`/`) with built-in error handling for division by zero.
- 🛡️ **Input Validation**: Prevents crashes from invalid operators.

---

## 🛠️ Requirements & Technologies

- **Language:** Java (JDK 8 or higher)
- **Tool / Environment:** Any standard Java Compiler or Online IDE (e.g., Programiz, Replit, VS Code, Eclipse, IntelliJ IDEA).

---

## 📄 Java Source Code (`Main.java`)

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("=== Simple Calculator ===");
        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();
        
        System.out.print("Enter an operator (+, -, *, /): ");
        char operator = scanner.next().charAt(0);
        
        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();
        
        double result = 0;
        boolean valid = true;
        
        switch(operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if(num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error! Division by zero is not allowed.");
                    valid = false;
                }
                break;
            default:
                System.out.println("Error! Invalid operator.");
                valid = false;
        }
        
        if(valid) {
            System.out.println("Result: " + num1 + " " + operator + " " + num2 + " = " + result);
        }
        
        scanner.close();
    }
}
```

---

## 🚀 How to Run

1. Copy the Java code above into a file named `Main.java`.
2. **Compile the Java code:**
   ```bash
   javac Main.java
   ```
3. **Run the application:**
   ```bash
   java Main
   ```

---

## 💻 Example Usage

```text
=== Simple Calculator ===
Enter first number: 4
Enter an operator (+, -, *, /): /
Enter second number: 9
Result: 4.0 / 9.0 = 0.4444444444444444
```

---

## 👩‍💻 Author

Created by **Esraa Ahmed** ✨  
*University Student at the College of Computer and Information Sciences*