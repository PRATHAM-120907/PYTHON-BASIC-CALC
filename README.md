def add(x, y):
    return x + y

def subtraction(x, y):
    return x - y

def multiplication(x, y):
    return x * y

def division(x, y):
    if y == 0:
        return "ERROR!!! DIVISION BY ZERO."
    return x / y

def calculator():
    while True:
        print("Choose the operation:")
        print("1) Addition")
        print("2) Subtraction")
        print("3) Multiplication")
        print("4) Division")
        print("5) Exit")
        choice = input("Enter your choice (1/2/3/4/5): ")
        
        if choice == "5":
            print("Exiting the calculator. Goodbye!")
            break
        
        if choice in ("1", "2", "3", "4"):
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))
        
            if choice == "1":
                print(f"THE RESULT IS: {add(num1, num2)}")
            elif choice == "2":
                print(f"THE RESULT IS: {subtraction(num1, num2)}")
            elif choice == "3":
                print(f"THE RESULT IS: {multiplication(num1, num2)}")
            elif choice == "4":
                print(f"THE RESULT IS: {division(num1, num2)}")
        else:
            print("INVALID INPUT!!!!")

if __name__ == "__main__":
    calculator()
