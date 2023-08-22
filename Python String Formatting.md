___
# PYTHON STRING FORMATTING
Links: [[Python]]
Status: #🌳 
Tags: [[Logging]]
<!--- Created on: 2023.08.23, 00:47 --->

- three alternatives to print nicely
___

# 1. String Concatenation:
   - Concatenate strings and variables using \`+\` operator.
   - Simple but less readable for complex formatting.
   ```python
name = "Nick"
pi = 3.14159265
print("Name: " + name + ", Age: " + str(age))
   ```

# 2. Formatted String Literals (f-strings):
   - Enclose expressions in curly braces within an f-string.
   - Clear and concise for embedding variables.
   ```python
name = "Nick"
pi = 3.14159265
print(f"{name} likes {pi}")
print(f"{name} likes {pi:.2f}") # rounded
   ```

# 3. String Formatting with %:
   - Use \`%\` operator with placeholders for variables.
   - Offers control over data types and formatting.
   ```python
name = "Nick"
pi = 3.14159265
print("Name: %s, Age: %d" % (name, pi))
   ```