# CS50 for Lawyers

### Programming Languages

##### Python
If you've never programmed before, not to worry! Do your best to
implement each program, but don't fret if you can't quite get all
three working. For these three exercises we'll use a site called
[repl.it](https://repl.it), which provides a lightweight online IDE for
writing simple programs. We recommend you log in using your
GitHub account at [repl.it](https://repl.it) before beginning (this will make it a
lot easier to find and rename your "repl"s if you need to go back),
but it is also okay to create so-called "repl"s anonymously.

---
Visit https://repl.it/@dlloyd09/CS50LawPseudorandom.
There you'll find a file started by Doug with some instructions
on how to get started and how to test your code. As soon as you
try to edit Doug's file, a new "repl" unique to you will be created.
In the file called main.py, implement a program that, quite simply,
prints a pseudorandom integer between 1 and 10, inclusive.
To figure out how, you might find Python's official documentation,
https://docs.python.org/3/library/random.html#functions-for-integers, or
Stack Overflow, https://stackoverflow.com/questions/3996904/generate-random-integers-between-0-and-9,
of particular help!

To submit your work, click "Share" at the top, and then under the "Invite" option, select "Copy repl link". Paste that link here. Do NOT select the "Post" option. Do NOT share your "join link", the latter is very likely to break, and therefore be inaccessible to the staff, if you share it with anyone else.

```Python
import random

#for i in range(20):
#  pseudorandom = random.randint(0, 10)
#  print(pseudorandom)

pseudorandom = random.randint(0, 10)
print(pseudorandom)

```
---
Visit https://repl.it/@dlloyd09/CS50LawGuess. After cloning that repl, in main.py, implement a program that picks a pseudorandom number between 1 and 10, inclusive, and asks the user to guess that number, giving them only one guess. Your program should then print some message, informing the user whether or not their guess was correct.

To submit your work, click "Share" at the top, and then under the "Invite" option, select "Copy repl link". Paste that link here. Do NOT select the "Post" option. Do NOT share your "join link", the latter is very likely to break, and therefore be inaccessible to the staff, if you share it with anyone else.
```Python
import random

print("Number Guessing Game\n")

#random.randint(lower limit, upper limit)
pseudorandom = random.randint(0, 10)

print("Pixie selected a number.")

flag = 0
while(flag==0):
  try:
    guess = int(input("Make a Guess: "))
    print("\n")
    flag=1
  except:
    print("Please enter an integer type numeric value.", end="\n\n")

if(pseudorandom==guess):
  print("Hurray! :)")
  print("Your guess is correct!")
  print("Pixie <3<3")
else:
  print("Bad Luck :(")
  print("Pixie selected '", end="")
  print(pseudorandom, end="")
  print("'")
```
---
Visit https://repl.it/@dlloyd09/CS50LawGame. After cloning that repl, in main.py, implement a program that picks a pseudorandom number between 1 and 10, inclusive, and gives the user up to 3 chances to guess that number, each time printing some message, informing the user whether or not their guess was correct. If the user guesses correctly at any point, the program should end.

To submit your work, click "Share" at the top, and then under the "Invite" option, select "Copy repl link". Paste that link here. Do NOT select the "Post" option. Do NOT share your "join link", the latter is very likely to break, and therefore be inaccessible to the staff, if you share it with anyone else.

```Python
import random

print("Number Guessing Game\n")

#random.randint(lower limit, upper limit)
pseudorandom = random.randint(0, 10)

print("Pixie selected a number.")
print("You have only 3 attempt to guess.", end="\n\n")

attempt = 2


for i in range(3):
  flag = 0
  while(flag==0):
    try:
      print("Attempt Remaining:", attempt, end="\n\n")
      guess = int(input("Make a Guess: "))
      flag=1
    except:
      print("Please enter an integer type numeric value.", end="\n\n")

  if(pseudorandom==guess):
    print("Hurray! :)")
    print("Your guess is correct!")
    print("Pixie <3<3")
    exit()
  else:
    print("Bad Luck :(", end="")
    if(attempt>0):
      print("\nPixie wants you to try again.", end="\n\n")
      attempt = attempt - 1
    elif(attempt==0):
      print(" Pixie selected '", end="")
      print(pseudorandom, end="")
      print("'")
```
