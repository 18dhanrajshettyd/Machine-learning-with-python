# Machine-learning-with-python

                                             Variables, expressions and statements

 Values and types
 
A value is one of the fundamental things like a letter or a number that a program manipulates. The values we have seen so far are 2 (the result when we added 1 + 1), and 'Hello, World!'.

These values belong to different types: 2 is an integer, and 'Hello, World!' is a string, so-called because it contains a "string" of letters. You (and the interpreter) can identify strings because they are enclosed in quotation marks.

The print statement also works for integers.

>>> print 4
4

If you are not sure what type a value has, the interpreter can tell you.

>>> type('Hello, World!')
<type 'str'>
>>> type(17)
<type 'int'>

Not surprisingly, strings belong to the type str and integers belong to the type int. Less obviously, numbers with a decimal point belong to a type called float, because these numbers are represented in a format called floating-point.

>>> type(3.2)
<type 'float'>

What about values like '17' and '3.2'? They look like numbers, but they are in quotation marks like strings.

>>> type('17')
<type 'str'>
>>> type('3.2')
<type 'str'>

They're strings.

When you type a large integer, you might be tempted to use commas between groups of three digits, as in 1,000,000. This is not a legal integer in Python, but it is a legal expression:

>>> print 1,000,000
1 0 0

Well, that's not what we expected at all! Python interprets 1,000,000 as a comma-separated list of three integers, which it prints consecutively. This is the first example we have seen of a semantic error: the code runs without producing an error message, but it doesn't do the "right" thing.

2.2 Variables
One of the most powerful features of a programming language is the ability to manipulate variables. A variable is a name that refers to a value.

The assignment statement creates new variables and gives them values:

>>> message = "What's up, Doc?"
>>> n = 17
>>> pi = 3.14159

This example makes three assignments. The first assigns the string "What's up, Doc?" to a new variable named message. The second gives the integer 17 to n, and the third gives the floating-point number 3.14159 to pi.

Notice that the first statement uses double quotes to enclose the string. In general, single and double quotes do the same thing, but if the string contains a single quote (or an apostrophe, which is the same character), you have to use double quotes to enclose it.

A common way to represent variables on paper is to write the name with an arrow pointing to the variable's value. This kind of figure is called a state diagram because it shows what state each of the variables is in (think of it as the variable's state of mind). This diagram shows the result of the assignment statements:



The print statement also works with variables.

>>> print message
What's up, Doc?
>>> print n
17
>>> print pi
3.14159

In each case the result is the value of the variable. Variables also have types; again, we can ask the interpreter what they are.

>>> type(message)
<type 'str'>
>>> type(n)
<type 'int'>
>>> type(pi)
<type 'float'>

The type of a variable is the type of the value it refers to.

Variable names and keywords

Programmers generally choose names for their variables that are meaningful     they document what the variable is used for.

Variable names can be arbitrarily long. They can contain both letters and numbers, but they have to begin with a letter. Although it is legal to use uppercase letters, by convention we don't. If you do, remember that case matters. Bruce and bruce are different variables.

The underscore character (_) can appear in a name. It is often used in names with multiple words, such as my_name or price_of_tea_in_china.

If you give a variable an illegal name, you get a syntax error:

>>> 76trombones = 'big parade'
SyntaxError: invalid syntax
>>> more$ = 1000000
SyntaxError: invalid syntax
>>> class = 'Computer Science 101'
SyntaxError: invalid syntax

76trombones is illegal because it does not begin with a letter. more$ is illegal because it contains an illegal character, the dollar sign. But what's wrong with class?

It turns out that class is one of the Python keywords. Keywords define the language's rules and structure, and they cannot be used as variable names.

Python has twenty-nine keywords:

and       def       exec      if        not       return
assert    del       finally   import    or        try
break     elif      for       in        pass      while
class     else      from      is        print     yield
continue  except    global    lambda    raise

You might want to keep this list handy. If the interpreter complains about one of your variable names and you don't know why, see if it is on this list.

Statements
 
A statement is an instruction that the Python interpreter can execute. We have seen two kinds of statements: print and assignment.

When you type a statement on the command line, Python executes it and displays the result, if there is one. The result of a print statement is a value. Assignment statements don't produce a result.

A script usually contains a sequence of statements. If there is more than one statement, the results appear one at a time as the statements execute.

For example, the script

print 1
x = 2
print x

produces the output

1
2

Again, the assignment statement produces no output.

Expressionsś
An expression is a combination of values, variables, and operators. A value all by itself is considered an expression, and so is a variable, so the following are all legal expressions (assuming that the variable x has been assigned a value):


17
x
x + 17
If you type an expression in interactive mode, the interpreter evaluates it and displays the result:

>>> 1 + 1
2
But in a script, an expression all by itself doesn’t do anything! This is a common source of confusion for beginners.
