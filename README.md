# Simple-Interesting-Calculator

logo = """
 _____________________
|  _________________  |
| | Pythonista   0. | |  .----------------.  .----------------.  .----------------.  .----------------. 
| |_________________| | | .--------------. || .--------------. || .--------------. || .--------------. |
|  ___ ___ ___   ___  | | |     ______   | || |      __      | || |   _____      | || |     ______   | |
| | 7 | 8 | 9 | | + | | | |   .' ___  |  | || |     /  \     | || |  |_   _|     | || |   .' ___  |  | |
| |___|___|___| |___| | | |  / .'   \_|  | || |    / /\ \    | || |    | |       | || |  / .'   \_|  | |
| | 4 | 5 | 6 | | - | | | |  | |         | || |   / ____ \   | || |    | |   _   | || |  | |         | |
| |___|___|___| |___| | | |  \ `.___.'\  | || | _/ /    \ \_ | || |   _| |__/ |  | || |  \ `.___.'\  | |
| | 1 | 2 | 3 | | x | | | |   `._____.'  | || ||____|  |____|| || |  |________|  | || |   `._____.'  | |
| |___|___|___| |___| | | |              | || |              | || |              | || |              | |
| | . | 0 | = | | / | | | '--------------' || '--------------' || '--------------' || '--------------' |
| |___|___|___| |___| |  '----------------'  '----------------'  '----------------'  '----------------' 
|_____________________|
"""
def add(n1, n2):
  return n1 + n2

def sub(n1, n2):
  return n1 - n2

def mul(n1, n2):
  return n1 * n2

def div(n1, n2):
  return n1 / n2

def calculation():
  repeat = False
  n1 = float(input("What's the first number?:"))
  while not repeat:
    operator = input("+\n-\n*\n/\nPick an operation:")
    n2 = float(input("What's the next number?:"))
    if operator == "+":
      ans = add(n1, n2)
      print(f'{n1} + {n2} = {ans}')
    elif operator == "-":
      ans = sub(n1, n2)
      print(f'{n1} - {n2} = {ans}')
    elif operator == "*":
      ans = mul(n1, n2)
      print(f'{n1} * {n2} = {ans}')
    elif operator == "/":
      ans = div(n1, n2)
      print(f'{n1} / {n2} = {ans}')
    else:
      print("Invalid operator")
    con = input(f"Type 'y' to continue calculating with {ans} or type 'n' to start a new calculation:\n")
    if con == "n":
      calculation()
    elif con == "y":
      repeat = False
      n1 = ans

print(logo)
calculation()
