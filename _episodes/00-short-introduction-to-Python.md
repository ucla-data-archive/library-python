---
title: "Python introduction"
teaching: 30
exercises: 15
questions:
- "What is Python?"
objectives:
- "Launch the Jupyter Notebook, create new notebooks, and exit the Notebook."
- "Create Markdown cells in a notebook."
- "Create and run Python cells in a notebook."
- "Short introduction to programminin Python"
keypoints:
- "Core concepts in python: Jupyter Notebook, data types, operators, functions."
---

# The Basics of Python

Python is a general purpose programming language that supports rapid development
of scripts and applications.

Python's main advantages:

* Open Source software, supported by Python Software Foundation
* Available on all platforms
* "Batteries Included" philosophy - libraries for common tasks available in
  standard installation
* Very large community

Python programs are plain text files.

* They have the .py extension to let everyone (including the operating system) know it is a Python program.
  * This is convention, not a requirement.
* It’s common to write them using a text editor but we are going to use the Jupyter Notebook.
* The bit of extra setup is well worth it because the Notebook provides code completion and other helpful features.
* Notebook files have the extension .ipynb to distinguish them from plain-text Python programs.
  * Can export as “pure Python” to run from the command line.

## Use the Jupyter Notebook for editing and running Python.

*   The [Anaconda package manager][anaconda] is an automated way to install the Jupyter notebook.
    *   See [the setup instructions]({{ page.root }}/setup/) for Anaconda installation instructions.
*   It also installs all the extra libraries it needs to run.
*   Once you have installed Python and the Jupyter Notebook requirements, open a shell and type:

~~~
$ jupyter notebook
~~~

This will start a Jupyter Notebook server and open your default web browser.

What happens is this:

1.   The server runs locally on your machine only and does not use an internet connection.
1.  The server sends messages to your browser.
1.   The server does the work and the web browser renders the notebook.
1.   You can type code into the browser and see the result when the web page talks to the server.

*   This has several advantages:
    *   You can easily type, edit, and copy and paste blocks of code.
    *   Tab complete allows you to easily access the names of things you are using
        and learn more about them.
    *   It allows you to annotate your code with links, different sized text, bullets, etc.
        to make it more accessible to you and your collaborators.
    *   It allows you to display figures next to the code that produces them
        to tell a complete story of the analysis.

![Example Jupyter Notebook](../fig/0_jupyter_notebook_example.jpg)  
*Screenshot of a [Jupyter Notebook on quantum mechanics](https://github.com/jrjohansson/qutip-lectures) by Robert Johansson*

> ## How It's Stored
>
> *   The notebook file is stored in a format called **JSON**.
> *   Just like a webpage, what's saved looks different from what you see in your browser.
> *   But this format allows Jupyter to mix source code, text, and images, all in one file.
{: .callout}

## The Notebook has Command and Edit modes.

*   Open a new notebook from the dropdown menu (that says 'New') in the top right corner of the file browser page.
*   Each notebook contains one or more cells that contain code, text, or images.

> ## Code vs. Text
>
> We often use the term "code" to mean
> "the source code of software written in a language such as Python".
> A "code cell" in a Notebook is a cell that contains software;
> a "text cell" is one that contains ordinary prose written for human beings.
{: .callout}

*   If you press <kbd>esc</kbd> and <kbd>return</kbd> alternately,
    the outer border of your code cell will change from gray/blue to green.
    *   The difference in color is subtle.
*   These are the command (gray) and edit (green) modes of your notebook.
*   In command mode, pressing the <kbd>H</kbd> key will provide
    a list of all the shortcut keys.
*   Command mode allows you to edit notebook-level features, and edit mode changes the content of cells.
*   When in command mode (esc/gray),
    *   The <kbd>B</kbd> key will make a new cell below the currently selected cell.
    *   The <kbd>A</kbd> key will make one above.
    *   The <kbd>X</kbd> key will delete the current cell.
    *   The <kbd>Z</kbd> key will undo your last cell deletion.
*   All actions can be done using the menus,
    but there are lots of keyboard shortcuts to speed things up.
*   If you remember the <kbd>esc</kbd> and <kbd>H</kbd> shortcut, you will be able to find out all the rest.

> ## Command Vs. Edit
>
> In the Jupyter notebook page are you currently in command or edit mode?  
> Switch between the modes.
> Use the shortcuts to generate a new cell.
> Use the shortcuts to delete a cell
>
> > ## Solution
> >
> > Command mode has a grey boarder and Edit mode has a green border.
> > Use <kbd>esc</kbd> and <kbd>enter</kbd> to switch between modes.
> > You need to be in command mode (Hit <kbd>esc</kbd> if your cell is green).  Type <kbd>B</kbd> or <kbd>A</kbd>.
> > You need to be in command mode (Hit <kbd>esc</kbd> if your cell is green).  Type <kbd>X</kbd>.
> >
> {: .solution}
{: .challenge}

## Use the keyboard and mouse to select and edit cells.

*   Pressing the <kbd>return</kbd> key turns the border green and engages edit mode,
    which allows you to type within the cell.
*   Because we want to be able to write many lines of code in a single cell,
    pressing the <kbd>return</kbd> key when in edit mode (green) moves the cursor to the next line in the cell just like in a text editor.
*   We need some other way to tell the Notebook we want to run what's in the cell.
*   Pressing the <kbd>shift</kbd> and the <kbd>enter</kbd> key together will execute the contents of the cell.
*   Notice that the <kbd>return</kbd> and <kbd>shift</kbd> keys on the
    right of the keyboard are right next to each other.

## The Notebook will turn Markdown into pretty-printed documentation.

*   Notebooks can also render [Markdown][markdown].
    *   A simple plain-text format for writing lists, links,
        and other things that might go into a web page.
    *   Equivalently, a subset of HTML that looks like what you'd send in an old-fashioned email.
*   Turn the current cell into a Markdown cell by entering
    the command mode (esc/gray) and press the <kbd>M</kbd> key.
*   `In [ ]:` will disappear to show it is no longer a code cell
    and you will be able to write in Markdown.
*   Turn the current cell into a Code cell
    by entering the command mode (esc/gray) and press the <kbd>Y</kbd> key.

## Markdown does most of what HTML does.

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
*   Use asterisks
*   to create
*   bullet lists.
~~~
  </div>
  <div class="col-md-6" markdown="1">
*   Use asterisks
*   to create
*   bullet lists.
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
1.  Use numbers
1.  to create
1.  numbered lists.
~~~
  </div>
  <div class="col-md-6" markdown="1">
1.  Use numbers
1.  to create
1.  numbered lists.
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
*  You can use indents
	*  To create sublists
	*  of the same type
*  Or sublists
	1. Of different
	1. types
~~~
  </div>
  <div class="col-md-6" markdown="1">
*  You can use indents
	*  To create sublists
	*  of the same type
*  Or sublists
	1. Of different
	1. types
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
# A Level-1 Heading
~~~
  </div>
  <div class="col-md-6" markdown="1">
# A Level-1 Heading
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
## A Level-2 Heading (etc.)
~~~
  </div>
  <div class="col-md-6" markdown="1">
## A Level-2 Heading (etc.)
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
Line breaks
don't matter.

But blank lines
create new paragraphs.
~~~
  </div>
  <div class="col-md-6" markdown="1">
Line breaks
don't matter.

But blank lines
create new paragraphs.
  </div>
</div>

<div class="row">
  <div class="col-md-6" markdown="1">
~~~
[Create links](http://software-carpentry.org) with `[...](...)`.
Or use [named links][data_carpentry].

[data_carpentry]: http://datacarpentry.org
~~~
  </div>
  <div class="col-md-6" markdown="1">
[Create links](http://software-carpentry.org) with `[...](...)`.
Or use [named links][data_carpentry].

[data_carpentry]: http://datacarpentry.org
  </div>
</div>

> ## Creating Lists in Markdown
>
> Create a nested list in a Markdown cell in a notebook that looks like this:
>
> 1.  Get funding.
> 2.  Do work.
>     *   Design experiment.
>     *   Collect data.
>     *   Analyze.
> 3.  Write up.
> 4.  Publish.
>
> > ## Solution
> >
> > This challenge integrates both the numbered list and bullet list.
> > Note that the bullet list is indented 2 spaces so that it is inline with the items of the numbered list.
> > ~~~
> > 1.  Get funding.
> > 2.  Do work.
> >     *   Design experiment.
> >     *   Collect data.
> >     *   Analyze.
> > 3.  Write up.
> > 4.  Publish.
> > ~~~
> {: .solution}
{: .challenge}

> ## More Math
>
> What is displayed when a Python cell in a notebook
> that contains several calculations is executed?
> For example, what happens when this cell is executed?
>
> ~~~
> 7 * 3
> 2 + 1
> ~~~
> {: .language-python}
>
> > ## Solution
> >
> > Python returns the output of the last calculation.
> > ~~~
> > 3
> > ~~~
> > {: .language-python}
> {: .solution}
{: .challenge}

> ## Change an Existing Cell from Code to Markdown
>
> What happens if you write some Python in a code cell
> and then you switch it to a Markdown cell?
> For example,
> put the following in a code cell:
>
> ~~~
> x = 6 * 7 + 12
> print(x)
> ~~~
> {: .language-python}
>
> And then run it with <kbd>shift</kbd>+<kbd>return</kbd> to be sure that it works as a code cell.
> Now go back to the cell and use <kbd>escape</kbd>+<kbd>M</kbd> to switch the cell to Markdown
> and "run" it with <kbd>shift</kbd>+<kbd>return</kbd>.
> What happened and how might this be useful?
>
> > ## Solution
> >
> > The Python code gets treated like markdown text.
> > The lines appear as if they are part of one contiguous paragraph.
> > This could be useful to temporarily turn on and off cells in notebooks that get used for multiple purposes.
> > ~~~
> > x = 6 * 7 + 12 print(x)
> > ~~~
> > {: .language-python}
> {: .solution}
{: .challenge}

> ## Equations
>
> Standard Markdown (such as we're using for these notes) won't render equations,
> but the Notebook will.
> Create a new Markdown cell
> and enter the following:
>
> ~~~
> $\sum_{i=1}^{N} 2^{-i} \approx 1$
> ~~~
>
> (It's probably easier to copy and paste.)
> What does it display?
> What do you think the underscore, `_`, circumflex, `^`, and dollar sign, `$`, do?
>
> > ## Solution
> >
> > The notebook shows the equation as it would be rendered from latex equation syntax.
> > The dollar sign, `$`, is used to tell markdown that the text in between is a latex equation.
> > If you're not familiar with latex,  underscore, `_`, is used for subscripts and circumflex, `^`, is used for superscripts.
> > A pair of curly braces, `{` and `}`, is used to group text together so that the statement `i=1` becomes the the subscript and `N` becomes the superscript.
> > Similarly, `-i` is in curly braces to make the whole statement the superscript for `2`.
> > `\sum` and `\approx` are latex commands for "sum over" and "approximate" symbols.
> {: .solution}
{: .challenge}

[anaconda]: https://docs.continuum.io/anaconda/install
[jupyter]: http://jupyter.org/
[markdown]: https://en.wikipedia.org/wiki/Markdown


## Introduction to Python built-in data types

### Strings, integers and floats

The most basic data types in Python are strings, integers and floats:

~~~
text = "Library Carpentry"
number = 42
pi_value = 3.1415
~~~
{: .source}

Here we've assigned data to variables, namely `text`, `number` and `pi_value`,
using the assignment operator `=`. The variable called `text` is a string which
means it can contain text characters such as letters and numbers. We could reassign the variable `text`
to an integer too - but be careful reassigning variables as this can get
confusing.

To print out the value stored in a variable we can simply type the name of the
variable into the interpreter:

~~~
text
~~~
{: .source}

~~~
"Library Carpentry"
~~~
{: .output}

However, in scripts we must use the `print` function:

~~~
# Comments start with #
# Next line will print out text
print(text)
~~~
{: .source}

~~~
"Library Carpentry"
~~~
{: .output}

### Operators

We can perform mathematical calculations in Python using the basic operators
 `+, -, /, *, %`:

~~~
2 + 2
~~~
{: .source}

~~~
4
~~~
{: .output}

~~~
6 * 7
~~~
{: .source}

~~~
42
~~~
{: .output}

~~~
2 ** 16  # power
~~~
{: .source}

~~~
65536
~~~
{: .output}

~~~
13 % 5  # modulo
~~~
{: .source}

~~~
3
~~~
{: .output}

We can also use comparison and logic operators:
`<, >, ==, !=, <=, >=` etc.
`and, or, not`

~~~
3 > 4
~~~
{: .source}

~~~
False
~~~
{: .output}

~~~
6 != 7
~~~
{: .source}

~~~
True
~~~
{: .output}

~~~
3 == 3
~~~
{: .source}

~~~
True
~~~
{: .output}

~~~
True and True
~~~
{: .source}

~~~
True
~~~
{: .output}

~~~
True or False
~~~
{: .source}

~~~
True
~~~
{: .output}

## Sequential types: Lists and Tuples

### Lists

**Lists** are a common data structure to hold an ordered sequence of
elements. Each element can be accessed by an index, where the first element is 0, the second element is 1, and so on:

~~~
numbers = [1,2,3]
numbers[0]
~~~
{: .source}

~~~
1
~~~
{: .output}

A `for` loop can be used to access the elements in a list or other Python data
structure one at a time:

~~~
for num in numbers:
    print(num)
~~~
{: .source}

~~~
1
2
3
~~~
{: .output}

**Indentation** is very important in Python. Note that the second line in the
example above is indented. This is Python's way of marking a block of code. We will
discuss this in more detail later.

To add elements to the end of a list, we can use the `append` method:

~~~
numbers.append(4)
print(numbers)
~~~
{: .source}

~~~
[1,2,3,4]
~~~
{: .output}

Methods are a way to interact with an object (a list, for example). We can invoke
a method using the dot `.` followed by the method name and a list of arguments in parentheses.
To find out what methods are available for an object, we can use the built-in `help` command:

~~~
help(numbers)
~~~
{: .source}

~~~
Help on list object:

class list(object)
 |  list() -> new empty list
 |  list(iterable) -> new list initialized from iterable's items
 ...
~~~
{: .output}

We can also access a list of methods available to an object using `dir`. Some methods names are
surrounded by double underscores. Those methods are called "special", and
usually we access them in a different way. For example `__add__` method is
responsible for the `+` operator.

~~~
dir(numbers)
~~~
{: .source}

~~~
['__add__', '__class__', '__contains__', ...]
~~~
{: .output}
