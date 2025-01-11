# Python Notes


### **Variables**
A variable is a named storage location in the computer's memory where you can store data. You can think of it as a container for holding information.

#### **Example:**
```python
name = "Alice"
age = 25
```
- Here, `name` is a variable holding the value `"Alice"`.
- `age` is a variable holding the value `25`.

---

### **2. Assigning Values to Variables**
You use the assignment operator `=` to store a value in a variable:
```python
variable_name = value
```
- **Left side**: The variable name.
- **Right side**: The value being assigned to the variable.

#### **Examples:**
```python
x = 10       # Integer
y = 3.14     # Float
name = "Bob" # String
is_happy = True  # Boolean
```

---

### **3. Using Variables with `input()` and `print()`**
You can use variables to store user input and display information.

#### **Example:**
```python
name = input("What is your name? ")
age = input("How old are you? ")

print("Your name is", name, "and you are", age, "years old.")
```

Output:
```
What is your name? Alice
How old are you? 25
Your name is Alice and you are 25 years old.
```

---

### **4. Variable Naming Rules**
In Python, variable names must follow specific rules:
1. **Must begin with a letter (a-z, A-Z) or an underscore (_).**
   - Valid: `name`, `_value`
   - Invalid: `1name`, `@value`

2. **Can contain letters, digits (0-9), and underscores.**
   - Valid: `age_1`, `user_name`
   - Invalid: `age-1`, `user-name`

3. **Cannot use Python keywords or reserved words.**
   - Reserved words include: `if`, `else`, `for`, `while`, `def`, `class`, etc.

4. **Case-sensitive.**
   - `Name` and `name` are different variables.

#### **Good Practices for Naming Variables:**
- Use descriptive names:
  ```python
  first_name = "Alice"
  total_score = 95
  ```
- Use snake_case for multi-word variable names:
  ```python
  user_name = "Bob"
  ```

---

### **5. Combining Variables, `input()`, and `print()`**
You can use variables to make your programs more interactive and readable.

#### **Example: Calculating Age in 10 Years**
```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))

future_age = age + 10
print(f"Hi {name}, you will be {future_age} years old in 10 years!")
```

Output:
```
Enter your name: Alice
Enter your age: 25
Hi Alice, you will be 35 years old in 10 years!
```

---

### **6. Tips for Working with Variables**
- **Always initialize variables** before using them:
  ```python
  count = 0
  ```
- **Use meaningful names** to improve code readability:
  ```python
  # Poor naming
  x = "Alice"
  y = 25

  # Better naming
  name = "Alice"
  age = 25
  ```

- **Be careful with data types when using variables**:
  ```python
  age = input("Enter your age: ")  # Returns a string
  age = int(age)  # Convert to an integer for calculations
  ```

### **Data Types and F-Strings in Python**

---

### **1. Data Types in Python**
Python supports several built-in data types, which can be grouped into the following categories:

#### **Basic Data Types**
1. **Integers (`int`)**: Whole numbers (e.g., `1`, `-100`, `42`).
   ```python
   age = 25  # Integer
   ```
2. **Floating-point numbers (`float`)**: Numbers with decimal points (e.g., `3.14`, `-0.01`).
   ```python
   pi = 3.14159  # Float
   ```
3. **Strings (`str`)**: Text data enclosed in quotes (e.g., `"hello"`, `'world'`).
   ```python
   name = "Alice"  # String
   ```
4. **Booleans (`bool`)**: Represents `True` or `False`.
   ```python
   is_student = True  # Boolean
   ```

#### **Composite Data Types**
1. **Lists (`list`)**: Ordered collections of items (e.g., `[1, 2, 3]`, `["a", "b", "c"]`).
   ```python
   fruits = ["apple", "banana", "cherry"]
   ```
2. **Tuples (`tuple`)**: Immutable ordered collections (e.g., `(1, 2, 3)`).
   ```python
   coordinates = (10.0, 20.0)
   ```
3. **Dictionaries (`dict`)**: Key-value pairs (e.g., `{"name": "Alice", "age": 25}`).
   ```python
   person = {"name": "Alice", "age": 25}
   ```

#### **Other Data Types**
1. **Set (`set`)**: Unordered collection of unique items (e.g., `{1, 2, 3}`).
2. **NoneType (`None`)**: Represents the absence of a value (`None`).

---

### **2. F-Strings (Formatted String Literals)**
F-strings provide a clean and concise way to format strings, introduced in Python 3.6. They allow embedding expressions directly into string literals.

#### **Syntax:**
```python
f"Your text {expression}"
```

- Start the string with `f` or `F`.
- Use curly braces `{}` to embed expressions, variables, or computations.

---

#### **Examples:**
1. **Basic Usage:**
   ```python
   name = "Alice"
   age = 25
   print(f"My name is {name} and I am {age} years old.")
   ```
   Output:
   ```
   My name is Alice and I am 25 years old.
   ```

2. **With Expressions:**
   ```python
   length = 5
   width = 3
   print(f"The area of the rectangle is {length * width}.")
   ```
   Output:
   ```
   The area of the rectangle is 15.
   ```

3. **Formatting Numbers:**
   - Control decimal places:
     ```python
     pi = 3.14159
     print(f"Pi rounded to 2 decimal places: {pi:.2f}")
     ```
     Output:
     ```
     Pi rounded to 2 decimal places: 3.14
     ```

   - Display as percentages:
     ```python
     accuracy = 0.98765
     print(f"Accuracy: {accuracy:.2%}")
     ```
     Output:
     ```
     Accuracy: 98.77%
     ```

4. **Aligning Text:**
   - Align to the left, right, or center:
     ```python
     print(f"{'Left':<10} {'Center':^10} {'Right':>10}")
     ```
     Output:
     ```
     Left       Center       Right
     ```

5. **Using Functions Inside F-Strings:**
   ```python
   name = "alice"
   print(f"Capitalized: {name.capitalize()}")
   ```
   Output:
   ```
   Capitalized: Alice
   ```

---

### **3. Combining Data Types and F-Strings**
F-strings work seamlessly with all Python data types.

#### **Example:**
```python
name = "Alice"
age = 25
grades = [85, 90, 92]

print(f"Name: {name}")
print(f"Age: {age}")
print(f"Grades: {grades}")
```
Output:
```
Name: Alice
Age: 25
Grades: [85, 90, 92]
```

---

### **4. Practical Example: F-Strings with Multiple Data Types**
Here’s how f-strings can simplify formatting:
```python
name = "Bob"
age = 30
height = 5.9
is_student = False

print(f"My name is {name}, I am {age} years old, and I am {height:.1f} feet tall.")
print(f"Am I a student? {is_student}")
```
Output:
```
My name is Bob, I am 30 years old, and I am 5.9 feet tall.
Am I a student? False
```

---

### **Key Benefits of F-Strings**
- **Readable:** Embeds variables and expressions directly in strings.
- **Efficient:** Faster than older methods like `str.format()` or string concatenation.
- **Flexible:** Supports all data types and complex expressions.

### **Random Module, Lists, For Loops, and the Range Function in Python**

---

### **1. Random Module**
The `random` module is used to generate random numbers or select items randomly.

#### **Key Functions:**
1. **`random.randint(a, b)`**:
   Generates a random integer between `a` and `b` (inclusive).
   ```python
   import random
   print(random.randint(1, 10))  # Random integer between 1 and 10
   ```

2. **`random.random()`**:
   Generates a random float between `0.0` and `1.0`.
   ```python
   print(random.random())  # Random float
   ```

3. **`random.choice(sequence)`**:
   Selects a random element from a list, tuple, or string.
   ```python
   colors = ["red", "blue", "green"]
   print(random.choice(colors))  # Randomly selects "red", "blue", or "green"
   ```

4. **`random.shuffle(sequence)`**:
   Shuffles the elements of a list in place.
   ```python
   numbers = [1, 2, 3, 4, 5]
   random.shuffle(numbers)
   print(numbers)  # Shuffled order
   ```

5. **`random.sample(sequence, k)`**:
   Selects `k` unique elements from a list.
   ```python
   numbers = [1, 2, 3, 4, 5]
   print(random.sample(numbers, 3))  # Randomly selects 3 unique elements
   ```

---

### **2. Lists**
A **list** is a collection of items that is ordered, changeable, and allows duplicates.

#### **Creating a List:**
```python
fruits = ["apple", "banana", "cherry"]
```

#### **Common Operations:**
1. **Accessing Elements:**
   ```python
   print(fruits[0])  # Output: apple
   ```

2. **Modifying Elements:**
   ```python
   fruits[1] = "blueberry"
   print(fruits)  # Output: ["apple", "blueberry", "cherry"]
   ```

3. **Adding Elements:**
   ```python
   fruits.append("orange")
   print(fruits)  # Output: ["apple", "blueberry", "cherry", "orange"]
   ```

4. **Removing Elements:**
   ```python
   fruits.remove("apple")
   print(fruits)  # Output: ["blueberry", "cherry", "orange"]
   ```

---

### **3. For Loops**
A **for loop** is used to iterate over a sequence (like a list, string, or range).

#### **Basic Example:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
Output:
```
apple
banana
cherry
```

#### **Using `enumerate()` in Loops:**
To access both the index and the value:
```python
for index, fruit in enumerate(fruits):
    print(f"Index: {index}, Fruit: {fruit}")
```
Output:
```
Index: 0, Fruit: apple
Index: 1, Fruit: banana
Index: 2, Fruit: cherry
```

---

### **4. `range()` Function**
The `range()` function generates a sequence of numbers.

#### **Syntax:**
```python
range(start, stop, step)
```
- **`start`**: Starting value (default is `0`).
- **`stop`**: Stopping value (exclusive).
- **`step`**: Step size (default is `1`).

#### **Examples:**
1. **Basic Range:**
   ```python
   for i in range(5):
       print(i)
   ```
   Output:
   ```
   0
   1
   2
   3
   4
   ```

2. **Custom Start and Step:**
   ```python
   for i in range(2, 10, 2):
       print(i)
   ```
   Output:
   ```
   2
   4
   6
   8
   ```

---

### **5. Combining Random, Lists, For Loops, and Range**
Here’s how these concepts can work together:

#### **Example 1: Randomly Populating a List**
Generate a list of 5 random integers between 1 and 10:
```python
import random

random_numbers = [random.randint(1, 10) for _ in range(5)]
print(random_numbers)
```

---

#### **Example 2: Simulating a Dice Roll**
Roll a six-sided die 10 times and store the results:
```python
import random

rolls = []
for _ in range(10):
    rolls.append(random.randint(1, 6))

print("Dice rolls:", rolls)
```

---

#### **Example 3: Shuffling and Iterating Over a List**
Shuffle a list of student names and print them in random order:
```python
import random

students = ["Alice", "Bob", "Charlie", "Diana"]
random.shuffle(students)

for student in students:
    print(student)
```

---

#### **Example 4: Generating and Summing Random Numbers**
Create a list of random numbers and calculate their sum:
```python
import random

numbers = [random.randint(1, 100) for _ in range(10)]
print("Random Numbers:", numbers)
print("Sum:", sum(numbers))
```
---

### **Laços `while` em Python**

O loop **`while`** é usado para executar um bloco de código repetidamente enquanto uma condição é verdadeira. Vamos explorar como funciona, com exemplos e dicas.

---

### **1. Estrutura Básica do `while`**

#### **Sintaxe:**
```python
while condição:
    # Código a ser executado enquanto a condição for verdadeira
```

- **`condição`**: Uma expressão que é avaliada como `True` ou `False`.
- O loop continua até que a condição se torne `False`.

#### **Exemplo Básico:**
```python
x = 0
while x < 5:
    print(x)
    x += 1
```
**Saída:**
```
0
1
2
3
4
```

---

### **2. Loops Infinito com `while`**
Se a condição nunca for `False`, o loop continuará para sempre.

#### **Exemplo de Loop Infinito:**
```python
while True:
    print("Este é um loop infinito!")
    break  # Use "break" para sair do loop
```

---

### **3. Palavras-Chave Úteis com `while`**
1. **`break`**: Sai do loop imediatamente.
   ```python
   count = 0
   while True:
       if count == 3:
           break
       print(count)
       count += 1
   ```
   **Saída:**
   ```
   0
   1
   2
   ```

2. **`continue`**: Pula para a próxima iteração do loop.
   ```python
   x = 0
   while x < 5:
       x += 1
       if x == 3:
           continue
       print(x)
   ```
   **Saída:**
   ```
   1
   2
   4
   5
   ```

3. **`else`**: Executa um bloco de código quando a condição do `while` se torna `False`.
   ```python
   x = 0
   while x < 3:
       print(x)
       x += 1
   else:
       print("Loop terminado.")
   ```
   **Saída:**
   ```
   0
   1
   2
   Loop terminado.
   ```

---

### **4. Exemplos Práticos**

#### **4.1. Contagem Regressiva**
```python
countdown = 10
while countdown > 0:
    print(f"Contagem regressiva: {countdown}")
    countdown -= 1
print("Fogo!")
```
**Saída:**
```
Contagem regressiva: 10
Contagem regressiva: 9
...
Contagem regressiva: 1
Fogo!
```

---

#### **4.2. Pedindo Entrada do Usuário**
Continuar pedindo uma entrada válida até que o usuário digite um valor aceitável.
```python
number = -1
while number < 0:
    number = int(input("Digite um número positivo: "))
print(f"Você digitou: {number}")
```

---

#### **4.3. Soma de Números**
Somar números inteiros fornecidos pelo usuário até que ele digite `0`.
```python
total = 0
while True:
    num = int(input("Digite um número (0 para parar): "))
    if num == 0:
        break
    total += num
print(f"Soma total: {total}")
```

---

#### **4.4. Gerando Números Aleatórios**
Usar um `while` para gerar números aleatórios até atingir um número específico.
```python
import random

target = 5
while True:
    num = random.randint(1, 10)
    print(f"Número gerado: {num}")
    if num == target:
        print("Número alvo alcançado!")
        break
```

---

### **5. Cuidados ao Usar `while`**
- **Condição Infinita**: Sempre garanta que a condição do `while` possa eventualmente se tornar `False`.
- **Debugging**: Use prints para entender o comportamento do loop.
- **Entradas do Usuário**: Valide entradas para evitar loops indesejados.

---

Making a test here.