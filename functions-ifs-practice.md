# More Practice with Functions and If Statements

## Functions
So we're going practice functions until we dream them at night. Functions are
blocks of code which contains a specific set of instructions when called. What
do you mean "when called"? Well after we create a function we have to explicitly
use the function so that the code will run. 

```python
print('Hey, I\'m the Pink Power Ranger') # We call the print function
```

In the above example we call the print function. A function is called by using
it's name and providing any arguments i.e. inputs, in this case the greeting
being printed. After we create our functions, we'll have to call them in the 
same way we call the print function

### Motivation
The king of all things prideful and vain implemented a new law: every string 
that's displayed in a program must be preceded by "For the glory of the King"
and succeeded by "He is mighty!". Let's see how it looks like

```python
# This is now illegal
print('JAXA is to Japan what NASA is to the USA') # Don't get locked up!

# This is exactly what we need to do
print('For the glrory of the King')
print('JAXA is to Japan what NASA is to the USA')
print('He is mighty!')
```
Now that the mad king has spoken, every single print statement must have those
lines as well, what a loser. We could type it every single time we print... but
that's so much effort. Even copying and pasting will get tedious over time. 
Luckily with functions there's an easier way to avoid to jail. 

```python
# Let's first define the function
def king_print(message):
    print('For the glrory of the King')
    print(message)
    print('He is mighty!')

# Now we can call it, just like what we do with print!
king_print('JAXA is to Japan what NASA is to the USA')
```

When you call the function you should see the following output

```
For the glrory of the King
JAXA is to Japan what NASA is to the USA
He is mighty!
```

Functions allow for high levels of code reusability. Any time we need to print
the extra lines, we simply have to call the function. We are writing better code
by repeating ourselves less. If you ever find yourself writing code that does 
the same thing in different parts of the program, you should make it a function.

Let's say the mad king wants to change the last line from "He is mighty!" to "He
is supreme!!!". We still want to avoid prison for a bad print statement, so we
need to change all our prints now! Luckily, since we have a function, we only
need to change the function definition. If we didn't have a function, we'd have
to change every single that prints "He is mighty!". Imagine if we printed that 
1000 times, yikes.

Let's look at another way to write the king_print function
```python
# Let's first define the function
def king_print2(message):
    print('For the glrory of the King\n' + message + '\nHe is mighty!')

# Let's call it again
king_print2('JAXA is to Japan what NASA is to the USA')
```

You should get the same exact output as `king_print`
```
For the glrory of the King
JAXA is to Japan what NASA is to the USA
He is mighty!
```

If we decided to share our function with other poor citizens, they won't really
care how we implement it (I mean sometimes they do, but most time they won't). 
All they need to know is the function name and what inputs to give it, in this 
case the string to be printed. This is abstraction, we're saving coders from 
the details of how it works. Think about it, do you know how the `print`
function works? You can learn how it does, but for your programs you don't need
to. 