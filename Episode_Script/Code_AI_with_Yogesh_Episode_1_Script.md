# Code AI with Yogesh — Episode 1
## Python for AI: Variables and Data Types

Estimated duration: 10–15 minutes with live typing, explanations, and practice pauses. Rehearse once to confirm timing.
Recording notes appear in square brackets and are not spoken.

## Cut 1 — Introduction
[Camera]

Do you want to learn Python to become an AI engineer? Then you are in the right place.

Hello, I’m Yogesh, and you’re watching Code AI with Yogesh.

In this playlist, we’ll learn Python from the basics, with a focus on the skills you’ll use to build AI applications.

If you’re a beginner, or you want to brush up on your Python, this series is for you. If you already know the basics, you can jump to the advanced videos as they become available.

Today, we’ll learn about variables and five basic data types. By the end of this video, you’ll be able to store information in Python, display it, and check its type.

Let’s start with examples from everyday life. Come with me to the whiteboard.

## Cut 2 — Understanding data types
[Whiteboard: write Text, Integers, Decimal numbers, True/False, No value]

Think about the different kinds of information we use every day.

First, we have text: a letter like A, a name like Ravi, or a sentence like “Welcome to Code AI with Yogesh.”

In Python, text is called a string, and its type is written as str. Even a single character is a string in Python.

Next, we have numbers without a fractional part: 1, 25, 567, zero, or negative numbers like minus 10.

These are called integers. In Python, their type is written as int.

For example, someone’s age or the number of messages in a conversation could be an integer.

Then we have numbers with a decimal point, such as 0.5, 45.74, or 234.563.

For these examples, we’ll use Python’s float type. A float can represent values such as a temperature or a model’s confidence score.

One small detail: floats are approximate, so some decimal values cannot be represented exactly. We’ll explore that later.

Next, we have values with only two possibilities: true or false.

For example: is the user logged in? Is the model ready?

In Python, these are Boolean values, and the type is written as bool. The values are True and False, with a capital T and a capital F.

Finally, sometimes we don’t have a value yet.

Imagine an AI application where the model has not generated a response. We can represent that missing value using None.

None is a special value, and its type is called NoneType. It is different from zero, False, or an empty piece of text.

[Show this summary]

| Kind of information | Python type | Example |
| --- | --- | --- |
| Text | str | "Yogesh" |
| Integer | int | 25 |
| Floating-point number | float | 0.95 |
| True or false | bool | True |
| No value | NoneType | None |

These are five basic types we’ll use today. Python has other types too, including lists and dictionaries, which we’ll learn in later videos.

Now, how do we store these values so we can use them in our code? That brings us to variables.

## Cut 3 — Variables and opening Colab
[Whiteboard]

You may remember examples like this from school:

x = 5
y = 7
z = x + y

Here, x and y are names for values. We use those names in an expression, and z becomes 12.

In Python, a variable is a name that refers to a value.

For example:

name = "Yogesh"
channel_name = "Code AI with Yogesh"

Here, name and channel_name are variable names. The text on the right contains the values we assign to them.

The equals sign means assignment: take the value on the right and assign it to the name on the left.

Why is this useful? Because we can give information a meaningful name and use it later, instead of typing the same value repeatedly.

We can also assign a new value to the same variable. We’ll see that in a moment.

[Switch to screen recording]

Let’s try this in Python.

For now, we’ll use Google Colab, which lets us run Python in a browser without installing Python on our computer. Its free option is enough for today’s examples.

Open colab.research.google.com and sign in with your Google account if prompted. Create a new notebook, and rename it “Python for AI — Episode 1.”

Click Connect to connect to a runtime. A runtime is the environment that executes our code.

Wait until it finishes connecting. The connection time can vary.

Once connected, we’re ready to write our first line of Python.

[Keep the Colab walkthrough brief. Record the interface you see; avoid promising a particular button colour or connection time.]

## Cut 4 — Live coding
### A. Displaying output with print()
[Use an existing code cell, or add one with + Code]

Our first function is print().

Think of it as a way to display information in the output below our code.

Type this:

```python
print("Welcome to Code AI with Yogesh")
```

Notice the parentheses after print. Inside them, we’ve written some text in double quotes.

The quotes tell Python that this is a string.

Click the play button next to the cell, or press Shift + Enter.

See? Our message appears below the cell. The quote marks are part of the code; they aren’t included in the displayed message.

Let’s try two more lines:

```python
print("Hello World")
print("Yogesh")
```

Remember: Python is case-sensitive. Use lowercase print. Writing Print with a capital P will cause an error in this example.

### B. Creating and using a string variable
[New cell]

Now let’s store some text in variables:

```python
name = "Yogesh"
channel_name = "Code AI with Yogesh"
introduction = "My name is Yogesh. I am an AI engineer."

print(name)
print(channel_name)
print(introduction)
```

These values are strings.

Notice something important: print(name) has no quotes around name. Python looks up the value assigned to that variable and displays it.

Compare these:

```python
print(name)
print("name")
```

The first line displays Yogesh. The second displays the actual word name.

Quotes make a difference!

Both single quotes and double quotes can be used for strings:

```python
city = 'Noida'
country = "India"

print(city)
print(country)
```

For now, we’ll mostly use double quotes. Just make sure the opening and closing quotes match.

### C. Integers and floats
[New cell]

Let’s create two integer variables:

```python
age = 25
message_count = 10

print(age)
print(message_count)
```

We don’t put these numbers inside quotes.

Now, let’s create two float variables:

```python
temperature = 28.5
confidence_score = 0.95

print(temperature)
print(confidence_score)
```

These values have a decimal point, so Python treats them as floats.

Compare these two values:

```python
number = 25
number_as_text = "25"
```

They may look similar when printed, but they have different types. The first is an integer, and the second is a string because it is inside quotes.

We’ll check that shortly.

### D. Booleans and None
[New cell]

For a Boolean value, use True or False:

```python
is_model_ready = True
is_user_logged_in = False

print(is_model_ready)
print(is_user_logged_in)
```

There are no quotes around True or False. If we wrote "True" in quotes, it would be a string.

Now, imagine our model hasn’t generated a response yet:

```python
ai_response = None

print(ai_response)
```

None represents the absence of a value here. Write it with a capital N and without quotes.

### E. Checking types
[New cell]

To check the type of a value, Python provides a built-in function called type().

We’ll put it inside print() so we can display every result:

```python
print(type(name))
print(type(age))
print(type(confidence_score))
print(type(is_model_ready))
print(type(ai_response))
```

[Run the cell and point to each result]

We get str, int, float, bool, and NoneType.

You’ll see each one displayed inside something like “class str.” For now, focus on the type name.

We didn’t have to declare the type when assigning these values. The values already have types, and our variable names refer to them.

Now let’s check our number example:

```python
print(type(number))
print(type(number_as_text))
```

The first is int. The second is str. This is why quotes matter.

### F. Reassigning a variable
[New cell]

A variable can refer to a new value:

```python
message_count = 10
print(message_count)

message_count = 11
print(message_count)
```

After the second assignment, message_count refers to 11.

Python also allows a variable name to refer to a value of a different type:

```python
example = 10
print(type(example))

example = "Ten"
print(type(example))
```

First, example refers to an integer. Then it refers to a string.

This is allowed, but in our applications, we’ll aim to use meaningful names consistently so our code stays easy to understand.

### G. A small AI application example
[New cell]

Let’s bring all five types together in an example:

```python
user_prompt = "Explain machine learning in simple words."
max_words = 100
confidence_score = 0.95
is_model_ready = True
ai_response = None

print("User prompt:", user_prompt)
print("Maximum words:", max_words)
print("Confidence score:", confidence_score)
print("Model ready:", is_model_ready)
print("AI response:", ai_response)
```

The prompt is a string, the word limit is an integer, the confidence score is a float, the model’s ready status is a Boolean, and the response is currently None.

We’re only storing sample values here. We haven’t connected to an AI model yet.

But you can already see how these basic Python concepts fit into an AI application.

## Cut 5 — Naming rules, practice, and closing
[Camera or screen]

Before we finish, let’s cover a few rules for variable names.

A variable name cannot contain spaces. For multiple words, use an underscore, like full_name or user_prompt.

It can contain letters, digits, and underscores, but it cannot start with a digit.

Python is case-sensitive, so name and Name are different variable names.

You also cannot use Python keywords, such as if or class, as variable names.

And avoid names like print or type, because we’re already using those as built-in functions.

For this series, we’ll use snake_case: lowercase words separated by underscores.

For example, full_name and confidence_score.

Another style is camelCase, such as fullName. Your optional homework is to look up the difference between snake_case and camelCase.

Your main practice task is to create five variables:

- Your name as a string.
- Your age as an integer.
- A temperature as a float.
- A Boolean called is_learning_python.
- A variable called ai_response with the value None.

Print each value and check its type using print(type(...)).

Then compare 25 with "25". Predict their types before running the code.

Pause the video and try it yourself.

Don’t be afraid of errors. Read the error message, check your code, and try again. Fixing small mistakes is part of learning to program.

Today, you learned how to create variables, display values with print(), and check five basic data types with type().

In the next episode, we’ll explore strings in more detail.

Text is central to many language-based AI applications: user prompts, documents, and AI responses are often strings.

Thanks for watching Code AI with Yogesh. See you in the next video!

---

## Notes for Yogesh
- Keep your natural speaking style; you don’t need to memorise every sentence.
- Type and run examples in order. Later cells depend on variables from earlier cells.
- A bare type(name) works in a notebook, but normally only the final expression in a cell is automatically displayed. Using print(type(...)) makes all five results visible.
- The five types introduced here are a starting point, not all of Python’s data types.
- Avoid saying “everything in AI is a string.” AI also uses numeric data, images, audio, tensors, and other representations.
- Shorten pauses or repeated explanations if your rehearsal exceeds 15 minutes.
- Colab’s free browser-based setup was checked against Google’s FAQ: https://research.google.com/colaboratory/intl/en-GB/faq.html

