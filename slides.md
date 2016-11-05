


# Week 4, Seminar 2: Getting Sass-y

- Understand the different Sass data types
- Understand what a mixin is and how to use it
- Understand how to use mixin arguments
- Understand best practices for refactoring Sass






Me on Wednesday: "We can store lots of different **things** as variables."

Me on Saturday: "Let's talk about what exactly those **things** are."

## Data types
- 4  data types: string, number, boolean, null
- 2 data structures: lists & maps




## Strings = text, in single or double quotes

'pizza'
"red"
'span'
"i like turtles"

## Numbers = numbers, with or without a unit

10
10px
8.11


## Booleans = a true or false value

true
false

** Note: No quotes! A boolean is not a string **


## Null = an empty value

null


# Data structures

## Lists = comma- or space-separated values

$border: 10px solid red;

$height, $width


## Maps = key-value pairs

$height:100px, $width:100px





# Mixins

- A mixin is a reusable piece of Sass code
- We use a mixin to _generate_ other Sass

- Syntax:
    At top of file:
      @mixin dimensions {
        height: 100px;
        width: 100px;
      }

    Wherever we want to use the mixin:
      @include dimensions;


## Mixin arguments

- An argument is a variable passed to a mixin
- Arguments help make our mixins dynamic

- Syntax:
    At top of file:
      @mixin mixin-name-here($size) {
        font-size: $size;
      }

    Wherever we want to use the mixin:
      @include mixin-name-here(24px);


## Mixins with Multiple Arguments

- Syntax:
    At top of file:
      @mixin dimensions($width, $height){
        width: $width;
        height: $height;
      }

    Wherever we want to use the mixin:
      @include dimensions(24px, 100px);


## Mixins with Fallback values

- Syntax:
    At top of file:
      @mixin dimensions($width: auto, $height: auto){
        width: $width;
        height: $height;
      }

    Wherever we want to use the mixin:
      @include dimensions($height: 200px);



## Tips for refactoring

- Use partials with the @import statement.
    **Separation of Concerns**

- Determine what elements/styles are often reused throughout your code. Create variables or mixins (whichever is appropriate) for these
    **Don't repeat yourself**

- Start with a simple mixin, then move to arguments
    **Avoid overly complex code**
