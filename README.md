 def calculator():
    print("Simple Calculator")
    print("Operations: +, -, *, /")
    num1 = float(input("Enter first number: "))
    operator = input("Enter operation: ")
    num2 = float(input("Enter second number: "))
    if operator == "+":
        print(f"Result: {num1 + num2}")
    elif operator == "-":
        print(f"Result: {num1 - num2}")
    elif operator == "*":
        print(f"Result: {num1 * num2}")
    elif operator == "/":
        print(f"Result: {num1 / num2}" if num2 != 0 else "Cannot divide by zero")
    else:
        print("Invalid operator")
 calculator()
