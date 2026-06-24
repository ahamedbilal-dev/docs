# Source: https://python.datalumina.com/control-flow/if-statements

## 

[​](https://python.datalumina.com/#what-are-if-statements)

What are if statements?

If statements let your program make decisions. They check if something is true or false, then act accordingly. Real-life logic:

- IF it’s raining THEN take umbrella
- IF battery < 20% THEN charge phone
- IF password correct THEN allow access

## 

[​](https://python.datalumina.com/#basic-if-statement)

Basic if statement

```
age = 18

if age >= 18:
    print("You can vote!")
    print("You're an adult")
```

How it works:

1. Check the condition (`age >= 18`)
2. If True, run the indented code
3. If False, skip it

The colon `:` and indentation are required! This is how Python knows what code belongs to the if statement.

## 

[​](https://python.datalumina.com/#if-else-statements)

If-else statements

Handle both True and False cases:

```
temperature = 25

if temperature > 30:
    print("It's hot!")
else:
    print("Nice weather!")
```

## 

[​](https://python.datalumina.com/#if-elif-else-chains)

If-elif-else chains

For multiple conditions:

```
score = 85

if score >= 90:
    print("A - Excellent!")
elif score >= 80:
    print("B - Good job!")
elif score >= 70:
    print("C - Keep it up!")
else:
    print("F - Need improvement")
```

Python checks each condition in order and runs the first True one.

Why `elif` instead of multiple `if` statements? With `elif`, Python stops checking once it finds a true condition. This is more efficient and prevents multiple blocks from running. The order matters - always put more specific conditions first!

## 

[​](https://python.datalumina.com/#multiple-conditions)

Multiple conditions

Combine conditions with `and`, `or`, `not`:

```
age = 25
has_license = True

# Both must be True
if age >= 18 and has_license:
    print("You can drive!")

# At least one must be True
if weekend or holiday:
    print("No work today!")

# Reverse the condition
if not raining:
    print("Let's go outside!")
```

## 

[​](https://python.datalumina.com/#nested-if-statements)

Nested if statements

Put if statements inside other if statements:

```
has_ticket = True
age = 15

if has_ticket:
    if age >= 18:
        print("Enjoy the movie!")
    else:
        print("Need adult supervision")
else:
    print("Buy a ticket first")
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting the colon

```
# Wrong
if x > 5
    print("Big")

# Right
if x > 5:
    print("Big")
```
Using = instead of ==

```
# Wrong (assignment)
if x = 5:
    print("Five")

# Right (comparison)
if x == 5:
    print("Five")
```
Wrong indentation

```
# Wrong
if True:
print("Hello")  # IndentationError

# Right
if True:
    print("Hello")
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now let’s learn about loops to repeat code efficiently!

[**Loops**\\ \\ Repeat code without copying](https://python.datalumina.com/basics/loops)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/control-flow/if-statements.mdx)

[Control flow](https://python.datalumina.com/control-flow) [Loops](https://python.datalumina.com/basics/loops)

Ctrl+I