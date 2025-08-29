                         Exercises ➞ Functions

//////////////    Exercises ➞ Level 1 //////////////

# Q1.
# def area_of_Circle(r):
#     area = 2 * 3.14 * r
#     print(area)

# r = int(input("Enter Radius of Circle: "))
# area_of_Circle(r)

# Q2.
# def add_all_nums(*args):
#     total = 0
#     for num in args:
#         total += num
#     print(total)

# add_all_nums(1,2,3,4,5)

# def add_all_function(*args):
#     total = 0
#     for item in args:
#         if not isinstance(item, (int,float)):   #checks whether an object is of aparticular type.
#             return f"Invalid input: {item} is not a number."
    
#     return sum(args)

# # add_all_function(1,2,3,4,5)
# print(add_all_function(10,"hello",20))


# Q3. temp conversion c to f.

# def convert_temp(c):
#     f = (c * 9/5) + 32
#     print(f)

# c = int(input("Enter Celcius: "))
# convert_temp(c)    


# def convert_temp(celcius):
#     return (celcius * 9/5) + 32

# try:
#     c = float(input("Enter celsius: "))
#     f = convert_temp(c)
#     print(f"{c}C = {f:.2f}F")
# except ValueError:
#     print("Invalid input")    

# Q.4

# def check_season(month):

#     month = month.lower()

#     if month in ["september", "october", "november"]:
#         return "Autumn"
#     elif month in ["december", "january", "february"]:
#         return "Winter"
#     elif month in ["march","april","may"]:
#         return "Spring"
#     elif month in ["june","july","august"]:
#         return "summer"
#     else:
#         return "Invalid Month Name."
    
# month = input("Enter Month: ")
# print(check_season(month))    

# Q5.
#  Write a function called calculate_slope which return the slope of a linear equation

# Slope of linear equation

#      y2-y1
# m = -------
#      x2-x1

# def calculate_slope(points):

#     coord = []

#     for point in points:
#         coord.append(point) # loop through points and collect x and y values

#     x1, y1 = coord[0]
#     x2, y2 = coord[1]

#     if x2 - x1 == 0:
#         return "Slope is undefined (vertical line)"
    
#     slope = (y2-y1) / (x2-x1)
#     return slope

# print(calculate_slope([(2,3), (4,7)]))

#  m = -a/b

# def calculate_slope(a,b):

#     if b == 0:
#         return "Slope is undefined (vertical line)"
#     return -a / b

# print(calculate_slope(8,4))


# Q6.
#  Quadratic equation is calculated as follows: ax² + bx + c = 0. 
#  Write a function which calculates solution set of a quadratic equation, solve_quadratic_eqn.
import math

def solve_quadratic_eqn(a, b, c):
    if a == 0:
        raise ValueError("Coefficient 'a' cannot be 0 for a quadratic equation.")

    discriminant = b**2 - 4*a*c
    if discriminant < 0:
        return []  # No real roots

    roots = []
    for sign in [1, -1]:
        root = (-b + sign * math.sqrt(discriminant)) / (2 * a)
        roots.append(root)

    return roots

# Example usage:
print(solve_quadratic_eqn(1, -3, 2))


# Q7. Declare a function named print_list. It takes a list as a parameter and it prints out each element of the list.

# cities = ["delhi", "gurgaon", "noida", "pune", "mumbai", "chennai"]

# def print_list(list):
#     for item in list:
#         print(item, end=" ")

# print_list(cities)
# print()        

# Q8. Declare a function named reverse_list. It takes an array as a parameter and it returns the reverse of the array (use loops).

# def reverse_list(arr):
#     reversed_arr = []
#     for i in range(len(arr) - 1, -1, -1):
#         reversed_arr.append(arr[i])
#     return reversed_arr

# user_input = input("Enyter numbers and give space: ")

# arr = [int(x) for x in user_input.split()]

# print("Reversed List: ",reverse_list(arr))


# Q9. Declare a function named capitalize_list_items. 
# It takes a list as a parameter and it returns a capitalized list of items

# def capitalize_list_items(s):
#     return s.upper()

# s = input("Enter the parameters: ")
# print(capitalize_list_items(s))

# Q10. Declare a function named add_item. It takes a list and an item parameters. 
# It returns a list with the item added at the end.
# food_staff = ['Potato', 'Tomato', 'Mango', 'Milk'] 
# print(add_item(food_staff, 'Fungi')) 
# #['Potato', 'Tomato', 'Mango', 'Milk', 'Fungi'] 
# numbers = [2, 3, 7, 9] 
# print(add_item(numbers, 5)) #[2, 3, 7, 9, 5]

# def add_item(lst, item):
#     lst.append(item)
#     return lst

# lst = input("Enter your list: ").split()
# item = input("Enter you item to add: ")

# print(add_item(lst, item))


# Q11. Declare a function named remove_item. It takes a list and an item parameters. 
#    It returns a list with the item removed from it.
#    food_staff = ['Potato', 'Tomato', 'Mango', 'Milk'] 
#    print(remove_item(food_staff, 'Mango'))  
#    ['Potato', 'Tomato', 'Milk'] 
#    numbers = [2, 3, 7, 9] 
#    print(remove_item(numbers, 3)) # [2, 7, 9]

# def remove_item(lst, item):
#     lst.remove(item)
#     return lst

# food_staff = ['Potato', 'Tomato', 'Mango', 'Milk']
# print(remove_item(food_staff, 'Mango'))


# Q12. Declare a function named sum_of_numbers. It takes a number parameter and it adds all the numbers in that range.
#    print(sum_of_numbers(5)) 
#    15 
#    print(sum_all_numbers(10)) 
#    55 
#    print(sum_all_numbers(100))
#    5050


def sum_of_numbers(n):
    total = 0
#     for i in range(1, n+1):
#         total = total + i
#     return total

# print(sum_of_numbers(5)) 

### Using While
    i = 1
    while i <= n:
        total = total + i
        i += 1
    return total   

print(sum_of_numbers(100))   


# Q13. Declare a function named sum_of_odds. It takes a number parameter and it adds all the odd numbers in that range.

# def sum_of_odds(n):
#     total = 0
#     for i in range(1, n+1, 2):
#         print(i,end=" ")
#         total = total + i
#     return total
    
# print(sum_of_odds(100))


# Q14. Declare a function named sum_of_even. It takes a number parameter and it adds all the even numbers in that - range.


# def sum_of_even(n):
#     total = 0
#     for i in range(2, n+1, 2):
#         print(i,end=" ")
#         total = total + i
#     return total
    
# print(sum_of_even(100))








/////////////////////    Exercises --> Level 2 //////////////////

# Q1. Declare a function named evens_and_odds. 
# It takes a positive integer as parameter and it counts number of evens and odds in the number.

def evens_add_odds(n):
    even = 0
    odd = 0

#     ////////////    For given Input    ////////
    for i in n:
        if i % 2 == 0:
            even += 1
        else:
            odd += 1
    return even, odd

n = [1,2,3,4,5,6,7,8,9]            

#     ///////////     For user Input   /////////

#     for i in range(1, n+1):
#         if i % 2 == 0:
#             even += 1
#         else:
#             odd += 1
#     return even, odd        

# n = int(input("Enter positive integers: "))

even_count, odd_count = evens_add_odds(n)

print("Even numbers:", even_count)
print("Odd numbers:", odd_count)


# Q2. Call your function factorial, it takes a whole number as a parameter and it return a factorial of the number


# With loop

# def fact(n):
#     fact = 1
#     for i in range(1, n+1):
#         fact *= i
#     print("Factorial is: ",fact)
# n = int(input("Enter n: "))
# fact(n)


# using recusive method

# def fact(n):
#     if (n == 0 or n == 1):
#         return 1
#     else:
#         return fact(n-1) * n
# n = int(input("Enter N: "))
# print(fact(n))









