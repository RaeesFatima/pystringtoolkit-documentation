# Getting started
Welcome to **pystringtoolkit!**

This page will guide you through installation, importing, and using every function in the library, grouped by category.

## Installation
Install the latest version from PyPI:

```bash
pip install pystringtoolkit
```

## Importing Functions
You can import individual functions:
```commandline
from pystringtoolkit import to_kebab_case
```
Or import multiple at once:
```
from pystringtoolkit import to_snake_case, remove_punctuation
```
## Function Reference & Examples
Below are all available functions, organized into categories.

### **Case Conversion utilities**

* to_snake_case(text) — Converts text to snake_case
```
from pystringtoolkit import to_snake_case

print(to_snake_case("Hello World!"))  # hello_world
```
* to_camel_case(text) — Converts text to camelCase
```
from pystringtoolkit import to_camel_case

print(to_camel_case("hello world"))  # helloWorld
```
* to_pascal_case(text) — Converts text to PascalCase
```
from pystringtoolkit import to_pascal_case

print(to_pascal_case("hello world"))  # HelloWorld
```
* to_kebab_case(text) — Converts text to kebab-case
```
from pystringtoolkit import to_kebab_case

print(to_kebab_case("Hello World"))  # hello-world
```
* to_upper_case(text) — Converts all letters to uppercase
```
from pystringtoolkit import to_upper_case

print(to_upper_case("hello"))  # HELLO
```
* to_lower_case(text) — Converts all letters to lowercase
```
from pystringtoolkit import to_lower_case

print(to_lower_case("Hello"))  # hello
```
* to_title_case(text) — Capitalizes the first letter of each word
```
from pystringtoolkit import to_title_case

print(to_title_case("hello world"))  # Hello World
```
* to_alternating_case(text) - Alternate the case of each character in a string.
```
from pystringtoolkit import to_alternating_case

print(to_alternating_case("yEsssssss"))   #YeSsSsSsS
```
* invert_cases(text) - Invert the case of each character in a string.
```
from pystringtoolkit.case_conversion import invert_cases

print(invert_cases("Hello")) #hELLO
```

### **Text Cleaning Functions**

* remove_punctuation(text) — Removes punctuation, keeping letters/digits
```
from pystringtoolkit import remove_punctuation

print(remove_punctuation("Hello, World!"))  # Hello World
```
* remove_whitespaces(text) — Removes all whitespace characters
```
from pystringtoolkit import remove_whitespaces

print(remove_whitespaces("a b c"))  # abc
```
* remove_extra_spaces(text) — Reduces multiple spaces to a single space
```
from pystringtoolkit import remove_extra_spaces

print(remove_extra_spaces("Hello   World"))  # Hello World
```
* truncate(text, length) — Cuts text after a given length, adding ellipsis if needed
```
from pystringtoolkit import truncate

print(truncate("Hello World", 5))  # Hello...
```
* contains_only_alpha(text) — Checks if string has only alphabetic characters
```
from pystringtoolkit import contains_only_alpha

print(contains_only_alpha("Hello"))     # True
print(contains_only_alpha("Hello123"))  # False
```
* remove_vowels - Remove all vowels from a string.
```
from pystringtoolkit.cleaners import remove_vowels

print(remove_vowels("Hello World"))
```
* remove_consonants - Remove all consonants from a string, keeping only vowels and non-alphabetic characters.
```
from pystringtoolkit.cleaners import remove_consonants

print(remove_consonants("Hello World"))
```
* strip_html_tags - Remove HTML tags from a given string.
```
from pystringtoolkit.cleaners import strip_html_tags

print(strip_html_tags("<div><span>Nested</span></div>"))    #"Nested"
```
### **String Generation Tools**

* slugify(text) — Converts text into a URL-friendly slug
```
from pystringtoolkit import slugify

print(slugify("Hello World!"))  # hello-world
```
* random_string(length) — Generates a random alphanumeric string of given length
```
from pystringtoolkit import random_string

print(random_string(8))  # Example: a1B9xYzQ
```
* reverse_string - Reverse the given string
```
from pystringtoolkit.generators import reverse_string

print(reverse_string("Hello"))  # "olleH"
```
### **Validators**
* is_numeric(text) - Validates if it is numeric
```
from pystringtoolkit.validators import is_numeric

print(is_numeric("123"))
```
* is_email(text) - Validates if it is email
```
from pystringtoolkit.validators import is_email

print(is_email("user@example.com")) #True
```
* is_alpha - Validates if it is alphabet only
```
from pystringtoolkit.validators import is_alpha

print(isalpha("pystringtoolkit")) #True
```
* is_palindrome - Check if a string is a palindrome (reads the same forwards and backwards), ignoring case and non-alphanumeric characters.
```
from pystringtoolkit.validators import is_palindrome

print(is_palindrome("A man, a plan, a canal, Panama"))
```
* test_are_anagrams - Check if two strings are anagrams of each other (contain the same letters in a different order), ignoring case and spaces.
```
from pystringtoolkit.validators import are_anagrams

print(are_anagrams("Listen", "Silent"))
```
### **Text Counting functions**
* char_frequency - Count the frequency of each character in a string.
``` 
from pystringtoolkit.counting import char_frequency

print(char_frequency("hello"))
```
* most_common_char - Find the most common character in a string.
```
from pystringtoolkit.counting import most_common_char

print(most_common_char("hello"))    #l
```
* word_count - Count the occurrences of each word in a string (case-insensitive).
```
from pystringtoolkit.counting import word_count

print(word_count("Hello hello world"))  #{'hello': 2, 'world': 1}
```
* unique_words - Return a list of unique words from the string (case-insensitive), preserving order.
```
from pystringtoolkit.counting import unique_words

print(unique_words("Hello hello world"))
```
