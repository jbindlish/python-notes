# My Python Notes

## Strings

A string is defined as "string" with the quotation marks.

## Comparison 

There is > and < and <= and >=, which compare 2 things, and they return True/False The greater than or equal to, and smaller than or equal to operators are >= and <=. They are the same as the strict greater than and smaller than operators, except that they return True when comparing equal numbers. Greater than and smaller than operators can also be used to compare strings lexicographically (the alphabetical order of words is based on the alphabetical order of their component letters). 

## IF STATEMENTS: 

You can use if statements to run code if a certain condition holds. If an expression evaluates to True, some statements are carried out. Otherwise, they aren't carried out. To perform more complex checks, if statements can be nested, one inside the other. This means that the inner if statement is the statement part of the outer one. This is one way to see whether multiple conditions are satisfied. 

## IF ELSE STATEMENTS 

The if statement allows you to check a condition and run some statements, if the condition is True. The else statement can be used to run some statements when the condition of the if statement is False. As with if statements, the code inside the block should be indented. Every if condition block can have only one else statement. In order to make multiple checks, you can chain if and else statements. Example: 

num = 3 
if num == 1:
       print("One") 
else: 
  if num == 2: 
    print("Two") 
  else: 
     if num == 3: 
        print("Three") 
     else: 
        print("Something else") 

However, in this previous example, the code is very unreadable. So, you can use Elif statements. 

## ELIF STATEMENTS 

Rewriting the previous example, 

num = 3 
if num == 1: 
  print("One") 
elif num == 2: 
  print("Two") 
elif num == 3: 
  print("Three") 
else: 
  print("Something else")

As you can see in the example above, a series of if elif statements can have a final else block, which is called if none of the if or elif expressions is True. 

## BOOLEAN LOGIC 

Boolean logic is used to make more complicated conditions for if statements that rely on more than one condition. Python's Boolean operators are and, or, and not. The and operator takes two arguments, and evaluates as True if, and only if, both of its arguments are True. Otherwise, it evaluates to False. The or operator also takes two arguments. It evaluates to True if either (or both) of its arguments are True, and False if both arguments are False. Unlike other operators we've seen so far, not only takes one argument, and inverts it. The result of not True is False, and not False goes to True.
Helpful link: https://www.youtube.com/watch?v=UvI-AMAtrvE

You can combine if statements using Operators. For example, this code lets you check whether the type is visa or amex without making 2 if statements. That's a plus in my book. 

type = input()
if type=="Visa" or type=="Amex": 
  print("accepted") 

This is the table for operator precedence:
 

## LISTS 

Lists are a very important part of python. They allow you to store many pieces of information within one place. A list is created using square brackets and commas. An item in a list can be called using their index in square brackets. For example, if my list was list = ["Hello", "There"], then I could call "Hello" using list[0], and "There" using list[1]. Note that the first item in the list's index is 0, not 1, as might be expected. You may want to assign an empty list, using list = []. Then, you can store information later. Here is a code example: fruits = ["apple", "cherry", "banana", "kiwi", "lemon", "pear", "peach", "avocado"] num = int(input()) if num<0 or num>7: print('Wrong number') else: print(fruits[num]) In this example, you can find the item in the list using the user input. There can be multiple item types in a list, like string, int, float, variable, lists, etc. There can be a list nested inside a list, and you can call their items using a double index. For example, number = 3 things = ["string", 0, [1, 2, number], 4.56] print(things[2][2]) would return the item that's at index 2, in the nested list. You can express matrices in this form, by calling a specific item. Example: 

m = [ [1,2,3], [4,5,6] ] 
print(m[1][2]) 

This returns the 3rd item in the 2nd row, 6. Some types, such as strings, can be indexed. For example, str = "What" print(str[3]). This will return the 4th letter, "t". Note: space also counts. 

## LIST OPERATIONS 

List Replacement You can replace an item at a certain index. This works across multiple item types. Here is example of replacement, it returns [7, 7, 5, 7, 7]. 

nums = [7,7,7,7,7] 
nums[2]=5 
print(nums) 

## List Addition 

Lists can also be added and multiplied. You can add it to another list, to merge them using the + operation. nums = [1, 2, 3] nums = nums + [4,5,6] This returns a merged list nums = [1, 2, 3, 4, 5, 6] 

## List Multiplication 

You can also multiply the list by 3, just like strings. It would be duplicated like this: nums = [1, 2] nums = nums * 3 Now, the list nums is [1,2,1,2,1,2], [1,2] written 3 times. 

## In operator 

The In operator is used to check if an item is in the list. It returns True or False. Note: It is also used to check if a string is a substring of another string. Some cases are exemplified. 

Numbers = [1, 2, 3] 
print(1 in words) 
print(0 in words) 
print(4 in words) 

This returns: True False False. This is useful for using if statements regarding lists. Here is an example of using an if statement, where you check if a number is in the list. 

items = [42, 88, 721, 12, 43, 22, 908] 
num = int(input())
if num in items: 
  print("bingo") 

You can use the not operator to change the result around. 

## List Functions
 
https://www.youtube.com/watch?v=MKpVFaeT6uk 

# Append Function 

The append function is a way to add an item to the end of a list. Here is an example: 

num = [1,2,3]
 num.append(4) 
print(num) 

This code returns [1,2,3,4]. Note that append is a method of the list class, and that is why there is a dot.

### Len Function 

The Len function is a way to count the number of items in a list. For example, 

num = [1,2,3] 
print(len(num)) 

This returns 3, because there are 3 items in the list. Using the len function, we can find the middle number's index in the list: 

items = [2, 4, 6, 8, 10, 12, 14] 
length = len(items) 
print(length//2).

### Insert function 

The insert function lets you insert an item at any point in the list. 

list = ["Jai", "Cool] 
index = 1 
list.insert(index, "is").

Now, the list words is ["Jai", "is", "Cool"]. 

Note 1: now, the "is" is at index, which is at index 1. 

Note 2: Note that insert has 2 parameters. (the method is like that) 

Note 3: everything after "is" was pushed right

### index function 

The index function finds the index of a list item. If there isn't that item in the list, the code raises a Value Error. 

## Few More Functions 

max(list): Returns the list item with the maximum value 
min(list): Returns the list item with minimum value 
list.count(item): Returns a count of how many times an item occurs in a list 
list.remove(item): Removes an object from a list 
list.reverse(): Reverses items in a list. - basically inverts it.

Additional note: In the list list=[5,4,3,2,1], 5 would be in the 0th place 4 would be in the first place 3 2nd place 2 3rd place 1 4th place.
 
## WHILE LOOPS 

While loops are used to repeat a block of code multiple times. You can set the amount of times using an index. You can use multiple statements in a while loop. For example, you can use an if loop. This might be useful in a game where you need to check for something constantly. break statement You can prematurely break a while loop using the break function. For example, you can break an infinite loop if some condition is met. You can create an infinite loop using: while True: code code code Note: using a break statement outside of a loop result in an error. continue statement The continue statement is another statement that can be used in a while loop. It jumps back to the top of the loop. Basically, the continue statement stops the current iteration and continues with the next one. Note: Once again, using this statement outside of a loop results in an error.

## For Loops 
The for loop is used to iterate over a given sequence, such as lists or strings. You can go through the sequence, and check something. Note: Similar to While loops, you can use break and continue. In this example, a for loop is used to count the sum in the list. list = [1, 2, 3, 4, 5, 6, 7, 8, 9] sum = 0 for n in list: sum +=n print(sum) The output is 45. 

## For vs. While 

Both, for and while loops can be used to execute a block of code for multiple times. It is common to use the for loop when the number of iterations is fixed. For example, iterating over a fixed list of items in a shopping list. The while loop is used in cases when the number of iterations is not known and depends on some calculations and conditions in the code block of the loop. Both, for and while loops can be used to achieve the same results, however, the for loop has cleaner and shorter syntax, making it a better choice in most cases

## RANGE 

The range() function returns a sequence of numbers. By default, it starts from 0, increments by 1, and stops before the specified number. In order to make it a list, you need to specifically transform it into a list. If range() is called with 1 argument, then it produces an object with values 0 to that argument. (one less) If it is called with two arguments, it produces values from the first to the second. For example, list(range(3,7)) = [3,4,5,6]. Range can also have a third argument, which determines the interval of the sequence produced, also called the step. For example, list(range(5, 20, 2)) = [5, 7, 9, 11, 13, 15, 17, 19]. The list can also decrease, with a negative interval. 

## RANGE IN FOR LOOPS 

The for loop is commonly used to repeat some code a certain number of times. This is done by combining for loops with range objects. For example, for i in range(5): print("hello!") Would print "hello!" 5 times.

## Re-Using Code 

Code reuse is a very important part of programming, in any language. Increasing code size makes it harder to maintain. For a large programming project to be essential, you must abide by the DRY principle. This stands for Don't Repeat Yourself. You can do this by using loops, functions, or modules. Note: Bad code is usually by the WET principle, which stands for Write Everything Twice or We Enjoy Typing. https://www.youtube.com/watch?v=r9cnHO15YgU 

## Functions 

Any statement that consists of a word followed by information in parenthesis is a function call. Some of these functions that we already learned are: print("Hello World") range(2,20) str(3) And much more. The words in front of the parentheses are function names, and the comma-separated values inside the parentheses are function arguments. In addition to the pre-defined functions, you can create your own functions using the def statement. def my_func(): print("GAS GAS GAS") my_func() Note that in this example, my_func() was called. Without this, nothing would happen, because you wouldn't use it. You must define functions before they are called, in the same way that you must assign variables before using them. For example, name = input() def welcome_message(nam): 
print("Welcome, " +str(nam)) welcome_message(name) In this example, a function is defined to greet someone. One argument is the name of the person, who is greeted.
  
###Function Arguments 

Most functions that we have learned so far have 0 arguments. (Apart from my example where I had a clever use of nam and name) Here is an example with arguments: def who(action): print("Who " + action + "?") who(asked) There can also be multiple arguments within the function. For example, def multiply(x,y): print(x*y) multiply(4,2) A function argument can be used as a variable within the function definition, but it will raise an error if used outside of it. Technically, parameters are the variables in a function definition, and arguments are the values put into parameters when functions are called. 

### Function Return

Certain functions canreturn a value that can be used later. For example:

def max(x,y):
       if x>y:
              return x
       elif y>x:
              return y
 
z=max(5,8)

In this example, 8 will be stored in z, because the function returned y, or 8. 

Any statement after the return statement in a function is not executed. 

Here is an example of some code utilizing the return function.

s = input()

def hashtagGen(text):
	
	text1 = text.replace(" ", "")
	text = "#" + text1
	return text

print(hashtagGen(s))


## Comments

Comments are annotations in the code to make it easier to understand. It is made using a # symbol, and all text after it in a line is ignored by the code executor. 

#comment here

## Docstrings

Documentation Strings, or Docstrings, serve a similar purpose with comments. 

'''
Paragraphs are the building blocks of papers. Many students define paragraphs in terms of length: a paragraph is a group of at least five sentences, a 	paragraph is half a page long, etc. In reality, though, the unity and coherence of ideas among sentences is what constitutes a paragraph. A paragraph is defined as “a group of sentences or a single sentence that forms a unit” (Lunsford and Connors 116). Length and appearance do not determine whether a section in a paper is a paragraph. For instance, in some styles of writing, particularly journalistic styles, a paragraph can be just one sentence long. Ultimately, a paragraph is a sentence or group of sentences that support one main idea. In this handout, we will refer to this as the “controlling idea,” because it controls what happens in the rest of the paragraph.
'''

# Functions as Objects

Although they are defined differently than other objects, functions are just like them. They can be assigned and reassigned to variables, and later be referenced by them. 

def return(stuff):
	return(stuff)
	
print = return

print(return("hewwo"))

The output of this is hewwo.

Functions can also be used as arguements of other functions.

def add(a, b)
	return a+b

def do_twice(func, x, y):
	return func(func(x,y), func(x,y))
	


	
