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
# ============================================================
# 14. Check whether a given number is Armstrong or not
# ============================================================
num = int(input("Enter a number: "))
sum_val = 0
temp = num
while temp > 0:
    digit = temp % 10
    sum_val += digit ** 3
    temp //= 10
if num == sum_val:
    print("Armstrong number")
else:
    print("Not an Armstrong number")

# Example:
# Enter a number: 153
# Armstrong number

print("\n--------------------------------------------\n")

# ============================================================
# 15. Display Armstrong numbers between 1 and 500
# ============================================================
for num in range(1, 501):
    sum_val = 0
    temp = num
    while temp > 0:
        digit = temp % 10
        sum_val += digit ** 3
        temp //= 10
    if num == sum_val:
        print(num)

# Output:
# 1 153 370 371 407

print("\n--------------------------------------------\n")

# ============================================================
# 16. Check whether a number is perfect number
# ============================================================
num = int(input("Enter a number: "))
sum_div = 0
for i in range(1, num):
    if num % i == 0:
        sum_div += i
if sum_div == num:
    print("Perfect number")
else:
    print("Not a perfect number")

# Example:
# Enter a number: 28
# Perfect number

print("\n--------------------------------------------\n")

# ============================================================
# 17. Display all perfect numbers between 1 and 1000
# ============================================================
for num in range(1, 1001):
    sum_div = 0
    for i in range(1, num):
        if num % i == 0:
            sum_div += i
    if sum_div == num:
        print(num)

# Output:
# 6 28 496

print("\n--------------------------------------------\n")

# ============================================================
# 18. Check whether a number is strong number
# ============================================================
num = int(input("Enter a number: "))
sum_fact = 0
temp = num
while temp > 0:
    digit = temp % 10
    fact = 1
    for i in range(1, digit + 1):
        fact *= i
    sum_fact += fact
    temp //= 10
if num == sum_fact:
    print("Strong number")
else:
    print("Not a strong number")

# Example:
# Enter a number: 145
# Strong number

print("\n--------------------------------------------\n")

# ============================================================
# 19. Display all strong numbers between 1 and 500
# ============================================================
for num in range(1, 501):
    sum_fact = 0
    temp = num
    while temp > 0:
        digit = temp % 10
        fact = 1
        for i in range(1, digit + 1):
            fact *= i
        sum_fact += fact
        temp //= 10
    if num == sum_fact:
        print(num)

# Output:
# 1 2 145

print("\n--------------------------------------------\n")

# ============================================================
# 20. Print reverse of a number and check if it’s palindrome
# ============================================================
num = int(input("Enter a number: "))
rev = 0
temp = num
while temp > 0:
    digit = temp % 10
    rev = rev * 10 + digit
    temp //= 10
print("Reversed number:", rev)
if num == rev:
    print("Palindrome number")
else:
    print("Not a palindrome")

# Example:
# Enter a number: 121
# Reversed number: 121
# Palindrome number

print("\n--------------------------------------------\n")

# ============================================================
# 21. Find sum of all even and odd digits in a given number
# ============================================================
num = int(input("Enter a number: "))
even_sum = 0
odd_sum = 0
while num > 0:
    digit = num % 10
    if digit % 2 == 0:
        even_sum += digit
    else:
        odd_sum += digit
    num //= 10
print("Sum of even digits:", even_sum)
print("Sum of odd digits:", odd_sum)

# Example:
# Enter a number: 12345
# Sum of even digits: 6
# Sum of odd digits: 9

print("\n--------------------------------------------\n")

# ============================================================
# 22. Check whether a given number is Harshad number
# ============================================================
num = int(input("Enter a number: "))
temp = num
sum_digits = 0
while temp > 0:
    sum_digits += temp % 10
    temp //= 10
if num % sum_digits == 0:
    print("Harshad number")
else:
    print("Not a Harshad number")

# Example:
# Enter a number: 18
# Harshad number

print("\n--------------------------------------------\n")

# ============================================================
# 23. Display all Harshad numbers between 1 and 100
# ============================================================
for num in range(1, 101):
    temp = num
    sum_digits = 0
    while temp > 0:
        sum_digits += temp % 10
        temp //= 10
    if sum_digits != 0 and num % sum_digits == 0:
        print(num)

# Output: Many numbers including 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 18, 20, etc.

print("\n--------------------------------------------\n")

# ============================================================
# 24. Display multiplication tables from 1 to 10
# ============================================================
for i in range(1, 11):
    print(f"\nTable of {i}:")
    for j in range(1, 11):
        print(f"{i} x {j} = {i * j}")

# Example:
# Table of 1
# 1 x 1 = 1
# 1 x 2 = 2
# ...
# Table of 10
# 10 x 10 = 100

print("\n--------------------------------------------\n")

# ============================================================
# 25. Print prime factors of a given number
# ============================================================
num = int(input("Enter a number: "))
print("Prime factors are:")
for i in range(2, num + 1):
    while num % i == 0:
        print(i)
        num //= i

# Example:
# Enter a number: 36
# Prime factors are: 2 2 3 3

print("\n--------------------------------------------\n")

# ============================================================
# 26. Find LCM of two numbers using loops
# ============================================================
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
max_num = max(a, b)
while True:
    if max_num % a == 0 and max_num % b == 0:
        print("LCM is:", max_num)
        break
    max_num += 1

# Example:
# Enter first number: 4
# Enter second number: 6
# LCM is: 12

print("\n--------------------------------------------\n")

# ============================================================
# 27. Find GCD of two numbers using loops
# ============================================================
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
gcd = 1
for i in range(1, min(a, b) + 1):
    if a % i == 0 and b % i == 0:
        gcd = i
print("GCD is:", gcd)

# Example:
# Enter first number: 36
# Enter second number: 60
# GCD is: 12

print("\n--------------------------------------------\n")

# ============================================================
# 28. Display the sum of series: 1 + 2 + 3 + ... + N
# ============================================================
N = int(input("Enter N: "))
sum_series = 0
for i in range(1, N + 1):
    sum_series += i
print("Sum =", sum_series)

# Example:
# Enter N: 5
# Sum = 15

print("\n--------------------------------------------\n")

# ============================================================
# 29. Display the sum of series: 1² + 2² + 3² + ... + N²
# ============================================================
N = int(input("Enter N: "))
sum_series = 0
for i in range(1, N + 1):
    sum_series += i ** 2
print("Sum =", sum_series)

# Example:
# Enter N: 3
# Sum = 14

print("\n--------------------------------------------\n")

# ============================================================
# 30. Display the sum of series: 1³ + 2³ + 3³ + ... + N³
# ============================================================
N = int(input("Enter N: "))
sum_series = 0
for i in range(1, N + 1):
    sum_series += i ** 3
print("Sum =", sum_series)

# Example:
# Enter N: 3
# Sum = 36
