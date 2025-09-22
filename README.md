def add(a,b):
    return a+b
def sub(a,b):
    return a-b
def mul(a,b):
    return a*b
def div(a,b):
    if b==0:
        return "Error! Division by zero."
    return a/b

while True:
    print("\n-------------------------------CALCULATOR------------------------------")
    print("1. Addition (+)")
    print("2. Substraction (-)")
    print("3. Multiplication (x)")
    print("4. Division (/)")
    print("5. Exit")

    choice=input("Enter your Choice:")
    if choice=="5" or choice=="Exit":
        print("Exiting Calculator...... Goodbye!")
        break
    if choice in ['1','2','3','4','Addition','Substraction','Multiplication','Division','addition','substraction','multiplication','division']:
        try:
            a=float(input("Enter first number:"))
            b=float(input("Enter second number:"))
        except ValueError:
            print("Invalid input! Please enter numbers only.")
            continue
        if choice=='1' or choice=='Addition' or choice=='addition':
            print('Result:',add(a,b))
        elif choice=='2' or choice=='Substraction' or choice=='substraction':
            print('Result:',sub(a,b))
        elif choice=='3' or choice=='Multiplication' or choice=='multiplication':
            print('Result:',mul(a,b))
        elif choice=='4' or choice=='Division' or choice=='division':
            print('Result:',div(a,b))

    else:
        print("Invalid Choice! Please enter again.")
