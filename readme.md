# CSCI Software Engineering Assignment 4, Markdown Documentation

Jak Mortensen 9-30-25 CSCI 322 Software Engineering

[GitHub Repository Link](https://github.com/jmortensenmtech/322_Assignment04)

The purpose of this assignment to compare the formatting of the outputs of `printf` in C and `print` in Python. 

> **Note**: Formatting outputs matters because it ensures readability and understanding. Being able to easily understand the output enhances usability and the overall user experience.

---

## Integer Formatting

### C99 printf

```c
int n = 42; 
printf("%5d\n", n);       // width 5, right-aligned 
printf("%+5d\n", n);      // width 5, show sign 
printf("%05d\n", n);      // width 5, pad with zeros 
return 0;
```

### Python print

#### Old-style % formatting

```python
n = 42 
print("%5d" % n)     # width 5, right-aligned 
print("%+5d" % n)    # width 5, show sign 
print("%05d" % n)    # width 5, pad with zeros 
```

#### F-strings

```python
n = 42 
print(f"{n:5}")      # width 5, right-aligned 
print(f"{n:+5}")     # width 5, show sign 
print(f"{n:05}")     # width 5, pad with zeros
```

**These all will output:**

```
   42 
  +42 
00042
```

---

## Float Formatting

### C99 printf

```c
float f = 3.14159; 
printf("%8.2f\n", f);     // width 8, 2 decimals 
printf("%08.2f\n", f);    // pad with zeros 
printf("%e\n", f);        // scientific notation 
return 0;
```

### Python print

#### Old-style % formatting

```python
f = 3.14159 
print("%8.2f" % f)  # width 8, 2 decimals
print("%08.2f" % f) # pad with zeros
print("%e" % f)     # scientific notation
```

#### F-strings

```python
f = 3.14159 
print(f"{f:8.2f}")  # width 8, 2 decimals
print(f"{f:08.2f}") # pad with zeros
print(f"{f:e}")     # scientific notation
```

**These all will output:**

```
    3.14
00003.14
3.141590e+00
```

---

## String Formatting

### C99 printf

```c
char *s = "Hello"; 
printf("%-10s!\n", s);   // left-aligned, width 10 
printf("%10s!\n", s);    // right-aligned, width 10 
return 0;
```

### Python print

#### Old-style % formatting

```python
s = "Hello" 
print("%-10s!" % s) # left-aligned, width 10
print("%10s!" % s)  # right-aligned, width 10
```

**C99 printf and Python % print will output:**

```
Hello     !
     Hello!
```

####  F-strings

```python
s = "Hello" 
print(f"{s:<10}!") # left aligned, width 10
print(f"{s:>10}!") # right aligned, width 10
print(f"{s:^10}!") # center aligned, width 10
```

**Python F-strings will output:**

```
Hello     !
     Hello!
  Hello   !
```

### Formatting Tips
- For `integers`, use specifiers in C and Python to determine width, signs, and padding. EX: adding a plus sign or leading zeros.
- For `Floats`, use format options in either language to set decimal places or change to scientific notation. EX: Displaying a number with two decimal places.
- For `strings`, use alignment options in either language to adjust positioning. EX: Aligning the text to the left or centering the text in a certain width.

---

## Comparison Table

| Type   | C Code                        | Python Code             | Output           |
|--------|-------------------------------|--------------------------|------------------|
| int    | `printf("%5d", 42);`          | `"%5d" % 42`             | `   42`          |
| int    | `printf("%+5d", 42);`         | `"%+5d" % 42`            | `  +42`          |
| int    | `printf("%05d", 42);`         | `"%05d" % 42`            | `00042`          |
| float  | `printf("%8.2f", 3.14159);`   | `"%8.2f" % 3.14159`      | `    3.14`       |
| float  | `printf("%e", 3.14159);`      | `"%e" % 3.14159`         | `3.141590e+00`   |
| string | `printf("%-10s!", "Hello");`  | `"%-10s" % "Hello"`      | `Hello     !`    |
| string | `printf("%10s!", "Hello");`   | `"%10s" % "Hello"`       | `     Hello!`    |

---

## Links to Official Documentation

- [C99 printf reference](https://en.cppreference.com/w/c/io/fprintf)
- [Python old-style % formatting](https://docs.python.org/3/library/stdtypes.html#printf-style-string)
- [Python f-strings](https://docs.python.org/3/reference/lexical_analysis.html#f-strings)

---

## Image

![Image](https://static1.makeuseofimages.com/wordpress/wp-content/uploads/2021/12/c-programming-vs-python-programming.jpg)