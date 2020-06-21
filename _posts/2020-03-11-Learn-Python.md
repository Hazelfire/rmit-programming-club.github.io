---
layout: post
title: Learn how to Program in Python
author: Sam Nolan
categories: [Workshops]
---

This workshop will teach the basics of Python Programming, even for people who
have never touched programming!

<!-- more -->


## Learning how to Program in Python
-----

![Python xkcd](https://imgs.xkcd.com/comics/python.png)

Python!

First of all, a disclaimer. The person who wrote this is a human, and there
may be technologies I am unaware of.

If you're here, you probably know what Python is, but before we go on:

### Is Python for you?
Python will not be for you if you want to do the following things:

- Build a website (Check out [HTML](https://www.w3schools.com/html/))
- Build a professional game (Check out [Game Maker](https://www.yoyogames.com/gamemaker) or [Unity](https://unity.com/) or [Godot](https://godotengine.org/))
- Build a Mobile Application (Check out [Android](https://developer.android.com/training/basics/firstapp) or [iOS](https://developer.apple.com/develop/) development)

Python will be for you if you want to:

- Try out Data Analytics (Check out [pandas](https://pandas.pydata.org/docs/) and [jupyter](https://jupyter.org/))
- Build a super intelligent AI to take over the world (Check out [tensorflow](https://www.tensorflow.org/))
- Build a professional web application (Check out [Django](https://www.djangoproject.com/))
- Build a simple game (Check out [PyGame](https://www.pygame.org/news))
- Build scripts to automate your life
- Learn the basics of programming to apply in some other language
- Prototype applications quickly
- Do better calculations
- Talk with those cool as nerds from the Programming Club

If python is for you, let's move on!

### Installing Python
Installing Python is pretty simple, just go to the 
[python website](https://www.python.org/downloads/) and it will tell you how 
it's done. Just get the newest version.


### Starting with Python
We'll be making a very simple text adventure in Python. We'll start with learning
how to print things, then how to get input from the user, then how to use that
input to respond to the user in more intelligent ways.

To start working with Python, open IDLE (which should be installed on your computer
after installing Python). You should get the "Python Shell". Type in `1 + 2` into
that shell and see if you get the universe is still in order.

Go File -> New File.

You should get a screen with a textbox on it and write the following into the text box:

```python
print("Hello World")
```

Then run the script (Run -> Run Module).

This should print `Hello World` to the console. Congratulations! You have managed
to write your first script! If you don't understand it, don't worry, you'll get
the hang of it soon.

### Printing more things
To print more things, add more print statements! Find the nearest person, get their
name and their star sign. 

As I'm writing this, I have a friend in the row in front of me that I've just
met named Daniel. His star sign is Pisces.

```python
print("Hello Daniel")
print("It's fantastic to meet a Pisces!")
```

Run the script!

### Getting input
Now, as much fun as printing things is, we probably need to start listening to
the user. As it turns out, users do like being listened to.

We can get input from the user by using the `input` method:

```python
name = input("What is your name? ")
print("Hello " + name)
# This is a comment, I can write anything after this and it is ignored
# name and star_sign are called "variables", and variables cannot have any spaces
# in their names, so we use underscores
star_sign = input("What is your star sign? ")
print("It's fantastic to meet a " + star_sign + "!")
```

Run it!

Keep in mind these names like `input`, `name`, `star_sign` and `print` are all
case sensative. This means that you must type them exactly as said, no `Name` or
`NAME`.

### Variables
Variables are places where you can store information throughout your program.
Every variable has a type, `name = input("What is your name? ")` gets input
from the user as a **string** (Which is the same as text) and puts it is the `name`
variable.

Variables can change value over time, for instance:

```python
# The variable starts off with a type of "string" (text). To change it into a number,
# we have to wrap it in the int function
my_money = int(input("How much money do you have? "))

print("Merry Christmas! Here's $1,000,000")
my_money = my_money + 1000000

# I need to change this back to a string, as you cannot add an int (number) to text
print("Now you have $" + str(my_money))
```

To type strings you can put the quotes around the text you want, e.g.

```python
print("100")
```

To type numbers, ignore the quotes

```python
print(100)
```

Try the following:

```python
print("Hello " + "World")
print("100" + "2")
print(100 + 2)
```

and finally

```python
print("100" + 2)
```

### If statements
My star sign is Cancer, and I honestly think that users to my application who
have the cancer star sign should get special treatement.

We can do this with an if statement. Here's an example:

```python
star_sign = input("What is your star sign? ")
if star_sign == "Cancer":
    print("Oh! So am I!")
else:
    print("That's awesome! " + star_sign + " is my equal second favourite star sign!")
```

Here's another example

```python
password = input("What's the password? ")

if password == "Sneaky Socks":
    print("Access Granted")
else:
    print("Access Denied")
```

### Fancy If Statements
You can nest if statements

```python
username = input("What's your username")

if username == "Slarty Barkfast":
  password = input("What's your password? ")
  if password == "Sneaky Socks":
      print("Access Granted")
  else:
      print("Invalid Password")
else:
  print("No such user")
```

and you can do multiple branches with elif

```python
weapon = input("Choose your weapon! ")

if weapon == "Sword":
  print("You brandish a mighty sword")
elif weapon == "Bow":
  print("May the odds be ever in your favour")
elif weapon == "Pen":
  print("You brandish the strongest weapon of all")
else:
  print("Hazaar, a " + weapon)
```



### Let's get to it
Let's start building this text adventure!

```python


# This is an import statement, it allows me to create random numbers, you'll
# see it used later
# https://piximus.net/media/15087/essays-written-in-programming-languages-1.jpg
import random

name = input("What is your name? ")
quest = input("What is your quest? ")
favcolor = input("What is your favourite color? ")

"""
Another way to do comments is to just put 3 quotes to start and end the comment,
all this is ignored.

I'm going to do an adventure that was inspired by a fantastic Dungeon master 
named Jason Fox.

https://www.blackgate.com/2017/11/06/modular-fox-trot-plays-dungeons-dragons/
"""


print("This is the best dungeon I've created yet")
# The text between the quotes is called a "string". Anything between two " is
# considered a string, but what if you want a " in your string? You can then
# use \" instead, "Escaping" the quote
print("Ok. You are standing at the entrance to a cave. A sign reads \"Welcome to Jason Caverns.\"")

action = input ("What do you do?")
if action == "Enter the cave":
    print("Suddenly, there's an earthquake and the ceiling collapses! Your entire party is killed")

else:
    # Although this possibility is not enumerated, I can infer what Jason's intent is
    print("Suddenly, there's a tsunami and you are drowned! Your entire party is killed!") 

# This generates a random number between 1 and 100
print("Your bodies will remain undiscoved for (roll, roll)")
years = random.randint(1,100)
print(str(years) + " years!")

```

### Do it again!
We've got our first text adventure! There are a lot of things we can do here,
and if you're in the tutorial feel free to ask around for how to do things.

One important thing is looping, that is, doing things again and again until
some condition is satisfied.

```python
we_are_there = input("Are we there yet? ")

# Before we used == to check whether two things are equal
# != is the opposite, and checks whether it is not equal
# it reads, while we_are_there does not equal "Yes"
while we_are_there != "Yes":
    we_are_there = input("Are we there yet? ")

print("Yay! Can we go home now?")
```

Run it! This keeps asking whether we are there until you say "Yes".

### Math
If you want to try out some math, clear out your file and put the following:

```python
print(1 + 2)
print(2 * 3)
# This is 2 to the power of 3 (2 cubed)
print(2 ** 3)
print(4 / 3)
# This is floor division, it divides and rounds down
print(4 // 3)
```


### Keep going!

Other resources that might be useful for writing your text adventure:

- [Python Strings](https://www.w3schools.com/python/python_strings.asp)
- [Official docs](https://docs.python.org/3/tutorial/)
- [Learn Python the hard way](https://www.amazon.com.au/Learn-Python-Hard-Way-Introduction/dp/0321884914)
- [Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
