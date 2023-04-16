---
aliases:
- /python/swift/html/development/2021/11/16/code-comments
author: Eric M. Baumel
categories:
- python
- swift
- html
- development
date: '2021-11-16'
description: Be a good coding citizen, and be kind to your future self.
layout: post
title: Code Comments
toc: false

---

## Code Comments

Be a good coding citizen, and be kind to your future self.

> This is yet another in a series of posts about development infrastructure basics.

Some developers feel that code should be self-commenting; that the code should speak for itself. This might be an ideal, but for mere mortals comments 
helps explain the code and help aid future developers, including the future you.

Stylistically, comments should be complete sentences. The first word should be capitalized, unless it is an identifier that begins with a lower case letter.

Comments should be made at the same level of indent as the code it is commenting.

Here are the basics of comments for Python, Swift and a number of other languages. 

### Python

For a single line code, Python ignores everything after the hash mark ‘#’ and up to the end of the line.

Inline comments occur on the same line of a statement, following the code itself. They are separated by two spaces from the statement. These begin with
a hash mark and a single whitespace character.

While PEP 8 https://www.python.org/dev/peps/pep-0008/#maximum-line-length advises keeping code at 79 characters or fewer per line, it suggests a max of 72 characters for inline comments and docstrings. If your comment 
is approaching or exceeding that length, then you’ll want to spread it out over multiple lines.

You can comment out a block of code by selecting the lines and pressing Ctrl+/ on PC, or Cmd+/ on Mac.


Docstring convention https://www.python.org/dev/peps/pep-0257/

Docstrings are documentation comments which provide documentations for functions, classes and modules. These are defined by a pair of triple quotes (“”” ), 
just below the function or class declaration.

This string will become the .__doc__ attribute of your function and will officially be associated with that specific method. 

There are tools (e.g., pdoc https://pdoc3.github.io/pdoc and pydoc https://docs.python.org/3/library/pydoc.html) that allow you to generate documentation from the multiline docstrings in your code.

Imports
(Not really about comments, but this is also good code hygiene.) 
Imports should be grouped from most generic to least generic:
Python standard library imports
third-party module or package imports
Code repository sub-package imports


Place a blank line between import sections. Alphabetize within each group.

Python filenames must have a .py extension and must not contain dashes (-). You can use underscores instead.


### Swift

Code Comments

Code after double slashes, //, or in between slash stars, /* */ are code comments and are ignored by the compiler.

Documentation Comments

Option+Cmd+/, tells Xcode to insert a documentation comment placeholder for us. When your text cursor is above a 
function it will automatically add placeholders for parameters and return type.

### C and C++

C++ uses // for single line and inline comments and the C style /* for multi line */ comments.  Some authors suggest ‘/*’  
and ‘/**/’ for multi line commenting out of code, so you can then toggle the comments by deleting the initial comment 
characters to uncomment the lines.

 "C-style" or "multi-line" comments are /* Comment */.

"C++-style" or "single-line" comments are // Comment.


### HTML

HTML comments are <!-- --> for both single and multi line.


### CSS

CSS comments are the C-style /* */


### JavaScript
JavaScript uses the same comment style as Swift: // for single lines and: /* For multi lines */

JSDoc comments are used to for documentation comments, as in Swift, immediately above the function call. These comments begin with /** and use tags 
starting with the “at” symbol, such as @constructor and @param . 

### YAML

YAML only supports single line comments, starting with the ‘#’ sign.


### JSON

Nope. There are no comments in json.


### Markdown

`<!--- Using 3 hyphens —->`

Alternative methods:

`[//]: # “Comment goes here.”`
`[//]: # (Comment goes here.)`

`[comment]: # (Yet another comment style.)`

### Jekyll

`{% comment %}`

    These lines are commented out.
    
`{% endcomment %}`

### Ruby

A single line comment starts with # character and they extend from # to the end of the line 

You comment multiple lines using =begin and =end syntax. These tokens should start at the beginning of the line and be the only thing on that line.


### SQL

SQL comments use /* For both inline comments and multi lines. */
Single line comments start with ‘—’, a double dash.


Now go forth and be excellent to each other (and youself).
