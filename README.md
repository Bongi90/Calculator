def add(x, y):
  """This function adds two numbers"""
  return x + y

def subtract(x, y):
  """This function subtracts two numbers"""
  return x - y

def multiply(x, y):
  """This function multiplies two numbers"""
  return x * y

def divide(x, y):
  """This function divides two numbers"""
  if y == 0:
    return "Error! Division by zero"
  return x / y

print("Select operation:")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

while True:
  choice = input("Enter choice(1/2/3/4): ")

  if choice in ('1', '2', '3', '4'):
    try:
      num1 = float(input("Enter first number: "))
      num2 = float(input("Enter second number: "))
    except ValueError:
      print("Invalid input. Please enter numbers.")
      continue

    if choice == '1':
      print(num1, "+", num2, "=", add(num1, num2))

    elif choice == '2':
      print(num1, "-", num2, "=", subtract(num1, num2))

    elif choice == '3':
      print(num1, "*", num2, "=", multiply(num1, num2))

    elif choice == '4':
      print(num1, "/", num2, "=", divide(num1, num2))
    
    next_calculation = input("Let's do next calculation? (yes/no): ")
    if next_calculation == "no":
      break
  else:
    print("Invalid input. Please enter 1, 2, 3, or 4")
