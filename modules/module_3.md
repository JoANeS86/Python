## Introduction to While Loops

A while loop allows you to repeatedly execute a block of code while a certain condition is true. You can use the **break**
statement to exit the loop prematurely, and the **continue** statement to skip to the next iteration of the loop without executing
the rest of the code in the current iteration.

<ins>Example 1</ins>:

Instantiate a counter and create a While Loop that prints "not there yet," increments x by 1, and prints x until x reaches 5.

    x = 0

    while x < 5:
        print('Not there yet, x=' + str(x))
        x = x + 1
        print('x=' + str(x))

<ins>Example 2</ins>:

    # Import the random module to be able to create a (pseudo) random number.
    
    import random
    
    number = random.randint(1,25)                   # Generate random number
    number_of_guesses = 0                           # Instantiate guess counter
    
    while number_of_guesses < 5:
        print('Guess a number between 1 and 25: ')  # Tell user to guess number
        guess = input()                             # Produce the user input field
        guess = int(guess)                          # Convert guess to integer
        number_of_guesses += 1                      # Increment guess count by 1
    
        if guess == number:                         # Break while loop if guess is correct
            break
        elif number_of_guesses == 5:                # Break while loop if guess limit reached
            break
        else:                                       # Tell user to try again
            print('Nope! Try again.')
    
    # Message to display if correct
    
    if guess == number:
        print('Correct! You guessed the number in ' + str(number_of_guesses) + ' tries!')
        
    # Message to display after 5 unsuccessful guesses
    
    else:
        print('You did not guess the number. The number was ' + str(number) + '.')

<ins>Example 3</ins>:

    i = 0
    while i < 10:
        if i % 3 != 0:
            print(i)
            i += 1
            continue
        i += 1

## Introduction to For Loops

For Loops are like While Loops, but instead of looping continuously until a condition is met, For Loops iterate over each
element of an iterable sequence, allowing you to perform an action or evaluation with each iteration.

The basic syntax of a For Loop is as follows:

    for item in iterable_sequence:
       # Code block to be executed for each value in iterable_sequence

Sometimes you need to perform a task a set number of times, but you don’t already have an iterable object to loop over.
Or, sometimes you need to generate a known, regular sequence of numbers. This is where the **range()** function is useful.

The range() function is a function that takes three arguments: start, stop, step. Its output is an object belonging to the
range class. If you only include one argument, it will be interpreted as the stop value. The start and step values by default
will be zero and one, respectively. If you include two arguments, they will be interpreted as the start and stop values (again,
with step being one by default). Note that the stop value is not included in the range that is returned.

<ins>Examples</ins>:

    for i in range(3):
       print(i)
    
    for n in range(2, 5):
       print(n)
    
    for even_num in range(2, 11, 2):
       print(even_num)













