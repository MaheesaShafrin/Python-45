# Python-45
Write a Python program to check that a string contains only a certain set of characters (in this case a-z, A-Z and 0-9).
import re

def is_allowed_specific_char(string):
    
    charRe = re.compile(r'[^a-zA-Z0-9]')
 
    match = charRe.search(string)
    
    return not bool(match)


print(is_allowed_specific_char("ABCDEFabcdef123450"))  
print(is_allowed_specific_char("*&%@#!}{"))            

Output:

True
False
