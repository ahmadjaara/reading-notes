# Random Module in Python

## When to use it?

when We want the computer to pick a random element in a given range

## Random functions:

The Random module contains some very useful functions:
- Randint
random.randint(x,y): 
 pick an element between  x>element>=y 
- Random

    random.random()

- Choice :
Generate a random value from the sequence

- Shuffle
shuffles the elements in list in place, so they are in a random order.

- Randrange
Generate a randomly selected element from range(start, stop, step)

# What is Risk Analysis in Software Testing?

The probability of any unwanted incident is defined as **Risk**.

In **Software Testing**, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to tes

## Why use Risk Analysis?
using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks
## Risk Assessment
![risk](/pic/risk.png "1")

# Test coverage 
I would say you are doing enough testing if the following is true:

- You rarely get bugs that escape into production, and
- You are rarely hesitant to change some code for fear it will cause production bugs.


so, the value of coverage analysis that it Will help you find which bits of your code aren't being tested.It's worth running coverage tools every so often and looking at these bits of untested code. Do they worry you that they aren't being tested? 

        If a part of your test suite is weak in a way that coverage can detect, it's likely also weak in a way coverage can't detect.

