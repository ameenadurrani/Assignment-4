
#  Explanation of the Code
 Step-by-step explanation of the code:

# Step 1: Variable Declaration



You declare variables to hold three integers (num1, num2, and num3) and a string (name).

```
num1 : int
num2 : int
num3 : int
name : str 
```
# Step 2: Taking Input from the User

The program prompts the user to input their name and three favorite numbers.

The input for numbers is cast to integers (int()), as input returns a string by default.
```
name = input("Enter your name: ")
num1 = int(input("Enter your first favorite number: "))
num2 = int(input("Enter your second favorite number: "))
num3 = int(input("Enter your third favorite number: "))

```
# Step 3: Greeting the User
A personalized greeting message is printed using the f-string format to include the user's name.
```
print(f"Hello, {name}! Let's explore your favorite numbers:")

```
# Step 4: Creating a List of Favorite Numbers
A list called fav_num is created, which holds the three favorite numbers entered by the user.
``` 
fav_num = [num1, num2, num3]

```

# Step 5: Checking if the Numbers Are Even or Odd
The program iterates over each number in fav_num to check if it is even or odd.

If the number is divisible by 2 (i % 2 == 0), it is even; otherwise, it is odd.

A tuple is created for each number, pairing the number with 'even' or 'odd'.

These tuples are then appended to the tuples_list.
```
tuples_list : list = []
for i in fav_num:
    if (i % 2 == 0):
        print(f"The number {i} is even.")
        tuple = (i, 'even')
    elif (i % 2 != 0):
        print(f"The number {i} is odd.")
        tuple = (i, 'odd')
    tuples_list.append(tuple)

```
# Step 6: Finding the Square of Each Number
This loop calculates the square of each number (i ** 2) and prints the result.

A tuple containing the number and its square is created and added to the squareList.
``` 
squareList : list = []
for i in fav_num:
    print(f"The number {i} and its square: ({i}, {i ** 2})")
    square = (i, i**2)
    squareList.append(square)

```
# Step 7: Calculating the Sum of the Numbers
The sum of the numbers in fav_num is calculated using sum() and stored in totalSum.

The result is printed.
```
totalSum = sum(fav_num)
print(f"Amazing! The sum of your favorite numbers is: {totalSum}")

```
# Step 8: Checking if the Sum is a Prime Number
The code checks whether totalSum is a prime number.
``` 
is_prime : bool = True
if totalSum > 1:
    for j in range(2, int(totalSum**0.5) + 1):
        if totalSum % j == 0:
            is_prime = False
else:
    is_prime = False

```
# Step 9: Printing Whether the Sum is Prime or Not
The program prints whether totalSum is prime or not based on the value of is_prime.

```
if is_prime:
    print(f"Wow, {totalSum} is a prime number!")
else:
    print(f"Wow, {totalSum} is not a prime number!")
```