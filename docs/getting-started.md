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
* is_alpha
```
from pystringtoolkit.validators import is_alpha

print(isalpha("pystringtoolkit")) #True
```
