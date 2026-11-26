# Python strings: practice exercises

Practice notebook from Virel Data Lab. Indexing, slicing and string methods, finishing with a small data cleaning task.

## Indexing and slicing

~~~python
brand="VIREL DIGITAL"
~~~

1. Print the first character

~~~python
print(brand[0])
# V
~~~

2. Print the last character

~~~python
print(brand[-1])
# L
~~~

3. Extract the name VIREL

~~~python
print(brand[0:5])
# VIREL
~~~

4. Extract the word Digital

~~~python
print(brand[5:])
# ' DIGITAL'  (starts with a space)
~~~

## String methods

~~~python
student = "   evance otieno   "
~~~

1. Remove unnecessary spaces

~~~python
print(student.strip())
# evance otieno
~~~

2. Convert the name to title case

~~~python
print(student.title())
# '   Evance Otieno   '
~~~

3. Convert the name to uppercase

~~~python
print(student.upper())
# '   EVANCE OTIENO   '
~~~

4. Replace otieno with student

~~~python
print(student.replace("otieno","student"))
# '   evance student   '
~~~

## Data cleaning

Clean all the names with a for loop and store the results in a new list.

~~~python
students = [
    "  JOHN",
    "mary ",
    " PETER ",
    "GRACE",
    "  james"
]

cleaned_students = []
for s in students:
    cleaned_students.append(s.strip().title())

print(cleaned_students)
# ['John', 'Mary', 'Peter', 'Grace', 'James']
~~~

## Notes

- Indexing starts at 0 and -1 is the last character.
- In a slice the end index is excluded, so `brand[0:5]` stops before position 5.
- `brand[5:]` starts at the space, which is why the output has a leading space. `brand[6:]` gives DIGITAL on its own.
- String methods return a new string and leave the original alone. `title()`, `upper()` and `replace()` keep the spaces, only `strip()` removes them.
- In the loop, `s.strip().title()` chains two methods to clean each name in one line.

## Running it

Open `Data_science_module_5.ipynb` in Google Colab or Jupyter and run the cells in order. Nothing to install.

Instagram: @virel_digital
