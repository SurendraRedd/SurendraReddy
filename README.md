# SurendraReddy
About me - Best Practises

# Python Coding Best Practises

- 👉 Best Practise 1 → **Using enumerate()** - Fetch elements from list

    ```python
    # List Variable
    example = ['use','enumerate','instead','of','iteration']

    # Ideal Way
    for i in range(len(example)):
        print(f"# {i + 1}: {example[i]}")
              
    # Enemurate
    for i, value in enumerate(example, 1):
        print(f"# {i}: {value}")
    ```

- 👉 Best Practise 2 → **Using zip()** - Fetch elements from multiple lists

    ```python
    # Lists 
    Employees = ['Employee1','Employee2','Employee3','Employee4']
    Age = [30,25,35,40]

    # Ideal Way
    for i in range(len(Employees)):
        employee = Employees[i]
        age = Age[i]
        print(f"Employee name is {employee} and age is {age}")
        
    # Pythonic way - zip
    for employee, age in zip(Employees, Age):
        print(f"Employee name is {employee} and age is {age}")2. Pair Iterables With zip()
    ```

- 👉 Best Practise 3 → **Using reversed()** - Fetch elements reversly

    ```python
    # Lists 
    Employees = ['Employee1','Employee2','Employee3','Employee4']

    # Ideal way
    for i in range(1,len(Employees) + 1):
        print(f"Approach 1 - Employee came to office after covid 19 is {Employees[-i]}")
    for employee in Employees[::-1]:
        print(f"Approach 2 - Employee came to office after covid 19 is {employee}")
        
    # Pythonic way - reversed()
    for employee in reversed(Employees):
        print(f"Using revered -  Employee came to office after covid 19 is {employee}")
    ```

- 👉 Best Practise 4 → **Using filter()** - Data Filtering

    ```python
    # List
    numbers = [1,2,3,4,5,6,7,8,9,10]

    #Ideal way
    for number in numbers:
        if number % 2:
            print(f"Odd Number : {number}")

    # Pythonic way - filter()
    for number in filter(lambda x: x %2, numbers):
        print(f"Odd Number : {number}")
    ```

- 👉 Best Practise 5 → **Using Chain()** - Concatenate values from lists

    ```python
    from itertools import chain

    #Lists
    oddValues = [1,3,5,7,9]
    evenValues = [2,4,6,8,10]

    # Ideal way
    values = oddValues + evenValues
    for value in values:
        print(f"value is : {value}")

    # Pythonic way - chain()
    for value in chain(oddValues, evenValues):
        print(f"value is : {value}")
    ```

- 👉 Best Practise 6 → **Using Dictionaries()** - Retrieve keys & values from dictionary

    ```python
    # Dict
    Employees = {"Employee1": 30, "Employee2": 35, "Employee3": 40, "Employee4": 45}

    #Ideal way
    for key in Employees:
        print(f"Employee Name is : {key}")
    for key in Employees.keys():
        print(f"Employee Name is : {key}")
    for value in Employees.values():
        print(f"Age is : {value}")
    for value in Employees:
        print(f"Age is : {Employees[value]}")
        
    #Pythonic way
    for key, value in Employees.items():
        print(f"Employee came to office after covid 19 is {key} and age is {value}")
    ```

- 👉 Best Practise 7 → **Using Comprehension()** - Comprehensions for lists, dictionaries & set

    ```python
    ### list
    numbers = [1,2,3,4,5,6,7,8,9,10]

    #Ideal way
    squaredNumbers = list()
    for square in numbers:
        squaredNumbers.append(square * square)
    print(squaredNumbers)

    #Using list comprehension
    squaredNumbers = [x * x for x in numbers]
    print(squaredNumbers)

    #Ideal way
    squaredNumbers = dict()
    for square in numbers:
        squaredNumbers[square] = square * square
        
    #Using list comprehension
    squaredNumbers = {x: x*x for x in numbers}
    print(squaredNumbers)

    #Ideal way
    squaredNumbers = set()
    for square in numbers:
        squaredNumbers.add(square)
    print(squaredNumbers)

    #Using list comprehension
    squaredNumbers = [x*x for x in numbers]
    print(squaredNumbers)
    ```

- 👉Best Practise 8 → **Using else clause** - For and While Loops

    ```python
    # For Loop
    for n in range(2, 10):
        for x in range(2, n):
            if n % x == 0:
                print( n, 'equals', x, '*', n/x)
                break
        else:
            # loop fell through without finding a factor
            print(n, 'is a prime number')

    # While Loop
    count = 2
    while (count < 1):     
        count = count+1
        print(count) 
        break
    else: 
        print("No Break")
    ```
