## Best Practices for Virtual Labs Experiment Development 

### Introduction
  This document lists the best pratices to be followed while developing a Virtual Lab  experiment.

### General Principles
   1. The core imperative is to organize complexity.
   2. Clarity and readability of code
   3. Do not repeat yourself. Never copy-and-paste code.
   4. Always try to leave the code you work on in a better
      state than before you started

### Keep the source clean
   1. Always delete unused code. Including variables and
      using statements
   2. Don't comment out code, delete it. We have source
      control to manage change
   3. Indent the code to make it look clean and
      readable. Use tabs not spaces
   4. Avoid too big lines. Break it into mutiple lines for
      better readability
      
### Coding Standards
  The Virtual Labs recommends Google’s coding standard for Javascript. 
  The standard can be accessed [here](https://google.github.io/styleguide/jsguide.html). 
  Coding conventions are style guidelines for programming.

  *They typically cover :*
  + Naming and declaration rules for variables and functions.
  + Rules for the use of white space, indentation, and comments.
  + Programming practices and principles.

  *Coding conventions secure quality :*
  + Improves code readability
  + Make code maintenance easier

### HTML Coding Standards
   1. All documents must be using the HTML5 doctype and the
      <html> element should have a "lang" attribute. The
      <head> should also at a minimum include "viewport" and
      "charset" meta tags.
   2. All HTML documents must use two spaces for indentation
      and there should be no trailing whitespace. HTML5
      syntax must be used and all attributes must use double
      quotes around attributes.
   3. Document the structure properly
   4. Indent nested elements properly
   5. Use double quotes for attributes
   6. Use meaningful class names
   7. Do not repeat same id's for different elements instead
      use classes
   8. Do not use underscores for classes instead use hyphens
   9. Do not use images for buttons instead use css fonts or
      bootstrap glyphicons
   10. Use alt attribute for images with proper
       naming/description for the image
   11. Do not include styles in html as inline or internal
       css instead use external stylesheets for each feature
       to make the html and css clean and maintainable.
   12. Insert external JavaScript files at the bottom of the
       body tag and external Style Sheets in the head tag
       for for better performance
   13. Order the external files in a correct order to avoid
       errors
   14. Do not include a direct server link of a external
       frameworks like(Jquery, D3 etc.,). Download and
       include it.
   15. Do not use deprecated html tags (center etc.,)
   16. Do not use break tags for spacing
   17. Do not use special characters ("<", "=" etc.,)
   18. Do not use line breaks with html tags

### CSS Coding Standards
   1. All CSS documents must use two spaces for indentation
      and files should have no trailing white space.
   2. Do not declare the css rules on one line 
   3. Align the properties and values with same space
   4. Use shorthand properties wherever possible
   5. Use browser specific css rules to work on all browsers
      (Mainly on firefox and chrome).  Always provide
      fallback properties for older browsers.
   6. Do not keep all styles in one stylesheet, instead
      create a different stylesheets to organize and
      maintain code
   7. Do not use pixels for units, instead use %, em, vw, vh
      for better scalability on all the devices
   8. Do not repeat. Write a modular code to reuse it
   9. Place all the common styles in a seperate stylesheet
      to reuse it in different templates.
   10. Use media queries at the end of the file
   11. Put spaces before { in rule declarations.
   12. Use hex color codes #000 unless using rgba()
   13. Use double quotes
   14. Try keep all selectors loosely grouped into modules
       where possible and avoid having too many selectors in
       one declaration to make them easy to override.

## JavaScript Coding Standards
### Code Indentation
    Always use 2 spaces for indentation of code blocks.

#### Naming Conventions
    1. Declare variable and function names with camelCase or
       underscore and follow the same format throughout the
       code
    2. The name should accurately describe what the thing
       does
    3. Do not use shortenings, only use well understood
       names
    4. If the name looks awkward, the code is probably
       awkward
    5. Global variables written in UPPERCASE (We don't, but
       it's quite common)
    6. Constants (like PI) written in UPPERCASE

#### Variables
    1. Declare all the variables on top
    2. Use constants where possible. Avoid magic strings.
    3. Use readonly where possible
    4. Avoid global variables
    5. Avoid many temporary variables.
    6. Never use a single variable for two different
       purposes.
    7. Keep scope as narrow as possible. (declaration close
       to use)

#### Methods
    1. It should only do one thing.
    2. It should be small (more than 10 lines of code is
       questionable).
    3. The number of parameters should be small.
    4. Global methods should validate all parameters.
    5. Assert expectations and throw an appropriate error if
       invalid.
    6. Avoid deep nesting of loops and
       conditionals. (Cyclomatic complexity).

#### Separation of data
    Do not include data directly in code, instead have a
    configuration setup to embed

#### General rules for simple statements:
    Always end a simple statement with a semicolon.
#### General rules for complex (compound) statements
    1. Put the opening bracket at the end of the first line.
    2. Use one space before the opening bracket.
    3. Put the closing bracket on a new line, without
       leading spaces.  

#### Object Rules
    General rules for object definitions: 
    1. Place the opening bracket on the same line as the
       object name
    2. Use colon plus one space between each property and
       its value.
    3. Use quotes around string values, not around numeric
       values.
    4. Do not add a comma after the last property-value
       pair.
    5. Place the closing bracket on a new line, without
       leading spaces.
    6. Always end an object definition with a semicolon.

### Files Naming Conventions
   1. Name a meaningful and appropriate names for files
   2. Use lowercase for filenames
   3. Don't use spaces in the filename instead use
      underscores for word seperation
   4. Same above conventions to be followed for naming
      images, videos etc.,


## Color/Themes
It is recommended to use the colors defined below for images and simulation. </br>
`#98CB3B`/`rgb(152, 203, 59)`</br>
![#98CB3B](https://via.placeholder.com/450x55/98CB3B/000000?text=+) </br>
`#176696`/`rgb(23, 102, 150)`</br>
![#176696](https://via.placeholder.com/450x55/176696/000000?text=+) </br>
`#2C9AD1`/`rgb(44, 154, 209)`</br>
![#98CB3B](https://via.placeholder.com/450x55/2C9AD1/000000?text=+) </br>
`#96A0A3`/`rgb(150, 160, 163)`</br>
![#98CB3B](https://via.placeholder.com/450x55/96A0A3/000000?text=+) </br>
`#FFFFFF`/`rgb(255, 255, 255)` `White`</br>
![#98CB3B](https://via.placeholder.com/450x55/FFFFFF/000000?text=+)

## Fonts
It is recommended to use the font-family : “Helvetica Neue”,Helvetica,Arial,sans-serif  for text in images and simulations. 
