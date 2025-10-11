# ============================================================
# 1. Print numbers from 1 to 10, but skip 5 using continue
# ============================================================
for i in range(1, 11):
    if i == 5:
        continue
    print(i)

# Output:
# 1
# 2
# 3
# 4
# 6
# 7
# 8
# 9
# 10

print("\n--------------------------------------------\n")

# ============================================================
# 2. Print numbers from 1 to 10, but stop at 7 using break
# ============================================================
for i in range(1, 11):
    if i == 7:
        break
    print(i)

# Output:
# 1
# 2
# 3
# 4
# 5
# 6

print("\n--------------------------------------------\n")

# ============================================================
# 3. Search for a number in a sequence; stop searching if found
# ============================================================
numbers = [3, 7, 1, 9, 5]
search = int(input("Enter number to search: "))

for num in numbers:
    if num == search:
        print("Number found!")
        break
else:
    print("Number not found!")

# Example Input/Output:
# Enter number to search: 7
# Number found!

print("\n--------------------------------------------\n")

# ============================================================
# 4. Display even numbers between 1 and 20, skipping multiples of 4
# ============================================================
for i in range(2, 21, 2):
    if i % 4 == 0:
        continue
    print(i)

# Output:
# 2
# 6
# 10
# 14
# 18

print("\n--------------------------------------------\n")

# ============================================================
# 5. Menu-driven calculator with default in switch
# ============================================================
print("Menu:")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

choice = int(input("Enter choice (1-4): "))
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

match choice:
    case 1:
        print("Result:", a + b)
    case 2:
        print("Result:", a - b)
    case 3:
        print("Result:", a * b)
    case 4:
        print("Result:", a / b)
    case _:
        print("Invalid choice!")

# Example Input/Output:
# Enter choice (1-4): 1
# Enter first number: 5
# Enter second number: 3
# Result: 8.0

print("\n--------------------------------------------\n")

# ============================================================
# 6. Check if a number is prime, terminate loop early using break
# ============================================================
num = int(input("Enter a number: "))

if num <= 1:
    print("Not a prime number.")
else:
    for i in range(2, num):
        if num % i == 0:
            print("Not a prime number.")
            break
    else:
        print("Prime number.")

# Example Input/Output:
# Enter a number: 7
# Prime number.

print("\n--------------------------------------------\n")

# ============================================================
# 7. Read numbers until -1 is entered, skip negative numbers using continue
# ============================================================
while True:
    n = int(input("Enter a number (-1 to stop): "))
    if n == -1:
        break
    if n < 0:
        continue
    print("You entered:", n)

# Example Input/Output:
# Enter a number (-1 to stop): 5
# You entered: 5
# Enter a number (-1 to stop): -3
# Enter a number (-1 to stop): 7
# You entered: 7
# Enter a number (-1 to stop): -1

print("\n--------------------------------------------\n")

# ============================================================
# 8. Print multiplication table for a given number, but stop when product exceeds 50
# ============================================================
n = int(input("Enter a number: "))

for i in range(1, 11):
    product = n * i
    if product > 50:
        break
    print(f"{n} x {i} = {product}")

# Example Input/Output:
# Enter a number: 7
# 7 x 1 = 7
# 7 x 2 = 14
# 7 x 3 = 21
# 7 x 4 = 28
# 7 x 5 = 35
# 7 x 6 = 42
# 7 x 7 = 49

print("\n--------------------------------------------\n")

# ============================================================
# 9. Demonstrate default case when no matching switch case exists
# ============================================================
day = int(input("Enter day number (1-7): "))

match day:
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case 4:
        print("Thursday")
    case 5:
        print("Friday")
    case 6:
        print("Saturday")
    case 7:
        print("Sunday")
    case _:
        print("Invalid day number!")

# Example Input/Output:
# Enter day number (1-7): 9
# Invalid day number!

print("\n--------------------------------------------\n")

# ============================================================
# 10. Count positive numbers entered by the user until 0 is entered
# ============================================================
count = 0
while True:
    n = int(input("Enter a number (0 to stop): "))
    if n == 0:
        break
    if n > 0:
        count += 1
print("Total positive numbers entered:", count)

# Example Input/Output:
# Enter a number (0 to stop): 4
# Enter a number (0 to stop): -2
# Enter a number (0 to stop): 7
# Enter a number (0 to stop): 0
# Total positive numbers entered: 2

print("\n--------------------------------------------\n")

# ============================================================
# 11. Calculate factorial of a number using while loop
# ============================================================
n = int(input("Enter a number: "))
fact = 1
i = 1

while i <= n:
    fact *= i
    i += 1

print("Factorial:", fact)

# Example Input/Output:
# Enter a number: 5
# Factorial: 120

print("\n--------------------------------------------\n")

# ============================================================
# 12. Generate Fibonacci series using while loop
# ============================================================
n = int(input("Enter number of terms: "))
a, b = 0, 1
count = 0

while count < n:
    print(a, end=" ")
    a, b = b, a + b
    count += 1

# Example Input/Output:
# Enter number of terms: 7
# 0 1 1 2 3 5 8

print("\n\n--------------------------------------------\n")

# ============================================================
# 13. Find and print all prime numbers between 1 and N
# ============================================================
N = int(input("Enter the range: "))

for num in range(2, N + 1):
    for i in range(2, num):
        if num % i == 0:
            break
    else:
        print(num)

# Example Input/Output:
# Enter the range: 20
# 2
# 3
# 5
# 7
# 11
# 13
# 17
# 19
