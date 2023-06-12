# Calculator2.0

This project is a simple calculator that can perform basic mathematical operations such as addition, subtraction, multiplication, and division. The calculator is implemented in Python and uses a dictionary to map the four basic mathematical operations to the corresponding functions. The calculator prompts the user for two numbers and then performs the operation that the user selects. The result of the operation is then printed to the console. The user can continue calculating with the result or start a new calculation.

Here are some of the key features of the project:

It is a simple and easy-to-use calculator.
It is implemented in Python, which is a popular and powerful programming language.
It uses a dictionary to map the four basic mathematical operations to the corresponding functions.
It allows the user to continue calculating with the result or start a new calculation.

Below you can find the explanation of the code.


print("Welcome to the Calculator")
#This line of code prints the message "Welcome to the Calculator" to the user.

def add(n1,n2):
    return n1 + n2
#This line of code defines a function called add. The function takes two numbers as input (n1 and n2) and returns the sum of the two numbers.

operations = {
    "+": add,
    "-": substract,
    "*": multiply,
    "/": divide
}
#This line of code creates a dictionary called operations. The dictionary maps the four basic mathematical operations to the corresponding functions.

def calculator():
    num1 = float(input("What's the first number: "))
    for op in operations:
        print(op)
#This line of code defines a function called calculator. The function prompts the user for the first number and then prints a list of the four basic mathematical operations.

should_continue = True
#This line of code creates a variable called should_continue and sets it to True. This variable will be used to determine whether the calculator should continue running.

calculation = operations[operation]
answer = calculation(num1,num2)

print(f"{num1} {operation} {num2} = {answer}")

if input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ") == 'y':
    num1 = answer
else:
    should_continue = False
    calculator()

#This loop will continue to run as long as should_continue is True. In each iteration of the loop, the user will be prompted to select an operation, enter the next number, and then the calculator will perform the operation and print the result. The user will then be prompted to either continue calculating with the result or start a new calculation. If the user chooses to continue calculating, the value of num1 will be updated with the result and the loop will continue. If the user chooses to start a new calculation, the value of should_continue will be set to False and the calculator will start over.
