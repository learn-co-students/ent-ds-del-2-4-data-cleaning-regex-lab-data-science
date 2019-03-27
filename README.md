
# Data cleaning with Regular Expressions - Lab


## Introduction
In the last lesson, we introduced a lot of new concepts. We introduced Regular Expressions, and showed how to use them to replace or retrieve information - from a DataFrame, a string or a file. In this lab, we're going to get some practice - first by writing regular expresssions to clean up strings, and then to apply transformations to information in a DataFrame and then finally to pull strings from a larger document. 

***Remember, it's a lab, so you need to fork it, clone it, `cd` into the directory and then open it up locally on your computer using `jupyter notebook`.***

## Objectives
You will be able to:
* Apply Regular Expressions to data stored within a string
* Apply Regular Expressions to data stored within a DataFrame
* Apply Regular Expressions to data stored within a file

## Cleaning up a String

Lets start by getting some practice making changes to a string using the `sub()` (substitutue) method in the Python `re` (regular expression) standard library. 

*Hint: Remember that you'll need to import the `re` library to make this work.*

Fullow the instructions in the cell below:


```python
content = "It's the end of the world as we know it, and I feel fine."
# Uncomment the line below this comment, and write the code to apply the sub() regex method to the content variable, 
# to create a new variable called "without_punctuation" that has the same text, but no apostrophes, commas or periods.
# without_punctuation = . . .
print(without_punctuation)
```

Great! Now in the cell below, take the original content variable and remove everything that isn't a letter (including spaces and punctuation).


```python
# your code goes here
print(without_punctuation_or_spaces)
```

Alright! Next up, in the cell below, remove everything that *is* a letter - just leave the spaces and punctuation. 


```python
# your code goes here
print(spaces_and_punctuation_only)
```

Looking good! In the following cell create and print two new variables - let's call them "vowels" and "consonants" and they should only contain the vowels (with spaces) and consonants (without spaces) from the varible below "a_well_known_phrase".


```python
a_well_known_phrase = "The quick brown fox jumps over the lazy dog"
# your code goes here
print(vowels)
print(consonants)
```

## Cleaning up a Column in a DataFrame

Alright! There is a csv in this directory. It's called "company_list.csv". In the cell below, write the code to import it into a DataFrame - lets call the DataFrame "companies" to reflect what it contains.

Great! Now write a script to take the FaxNumber column, and to remove any non-numeric characters.

Now write a script to strip non-numeric characters from the AnnualRevenues, and then to change the data type to integer and display the mean AnnualRevenues for a company on this list. 

***What is the mean revenue for a company on this list according to the data in the spreadsheet?***

## Importing and Retrieving Substrings from a Larger File

There's a text file called `macbeth.txt` in this project directory. Open and read the file into a variable called macbeth.

OK, now we have the text of Macbeth, lets find all of the references to the following characters:
Lady, King, Malcome, Donalbaine, Lenox, Witches, Captaine, Banquo

Return a list that contains every match to any one of those strings.

And for bonus points (not required!), see if you can write a script that counts the number of each mentions and returns something similar to a dictionary with the number of mentions of each word. It should look something like:

{'King': 12, 'Lady': 12, 'Banquo': 12, 'Lenox': 12, 'Witches': 12, 'Donalbaine': 12, 'Captaine': 12, 'Malcome': 12}

Hint, there's a special library you can import - the syntax is `from collections import Counter` - see if you can Google to figure out how to use it!

## Summary

Congratulations! Just a couple of weeks ago you probably didn't even have Python installed and now you're using it to import and clean up all kinds of different data sets! Next up, we're going to start to look into API's (Application Programming Interfaces) and how we can use them to retrieve data to work on!
