## Best Practices for Virtual Labs Experiment Development 

### Introduction
  This document lists the best pratices to be followed while developing a Virtual Lab  experiment.

### General Principles
   It is imperative to
   1. Organize complexity
   2. Maximize clarity and readability of code
   3. Optimize usability and performance
   4. Review early, test frequently
   5. Follow standards and keep the code compliant with latest standards
   6. Use open-source libraries with large communities and active development and support
   7. Use mature tools that are fit for the task at hand
      
### Architecture Style
   1. Make the experiments into static sites
   2. Use server-side components only when there's no alternative
   3. Add dynamic functionality through services

### Performace and Usability
   1. Write code for mobile form-factor and expand it to work on larger screens
   1. Performance should be a fore-thought, not an after-thought
   1. Use light-weight, high performance libraries
   1. Always keep the target audience in mind. Our primary users are from India with inconsistent network speeds and low-powered mobile devices

### Keep the source clean
   1. Always delete unused code. Including variables and
      using statements
   2. Don't comment out code, delete it. We have source
      control to manage change
   3. Indent the code to make it look clean and
      readable.
   4. Avoid too big lines. Break it into mutiple lines for
      better readability
   5. Keep functions small and focused on a single task.
   6. Refactor repeated code into separate functions so you do not repeat yourself.
      
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
   1. Use the the HTML5 doctype in all documents and make sure
      that the <html> element has a  "lang" attribute.  Make sure 
      that the <head> at a minimum includes "viewport" and
      "charset" meta tags.
   2. Use two spaces for indentation in all HTML documents
      and ensure that there are no trailing whitespace.  Use HTML5
      syntax and use double quotes around attributes.
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
   12. Prefer SASS(scss) over CSS for properly nested, easy to read code.
   13. Insert non-essential external JavaScript files at the bottom of the
       body tag and essential external Javascript and external Style Sheets in the head tag
       for for better performance
   14. Order the external files in a correct order to avoid
       errors
   15. Evaluate performance of CDNs for common libraries like Bootstrap, JQuery etc. Sometimes downloading them and linking from your own server is faster because many CDNs do not have servers in India.
   16. Strictly use HTML5 tags. With HTML5, html has moved to completely being a markup for explaining the structure of a document(semantic markup vs presentational markup). CSS is used for styling. All HTML tags used for styling are 'not recommended' in HTML5
   17. Do not use <br> for vertical spacing. Use css classes to add padding/margin instead. Use <br> to show logical separation in content, when required
   18. Do not use special characters ("<", "=" etc.,)
   19. Do not use HTML elements like <b>, <i> etc, instead use the tags which carry some semantics with them, e.g. <em>, <strong>, <mark>, <cite>, <dfn> etc

### CSS Coding Standards
   1. Use two spaces for indentation in all CSS documents
      and ensure that there are no trailing whitespace. 
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
       code.
    2. Make sure that the name accurately describes the
       variable's need.
    3. Do not use short forms; only use well understood
       names.
    4. Write global variables in UPPERCASE 
    5. Write constants (like PI) in UPPERCASE

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
   1. Ensure that it is small (more than 10 lines of code is
      questionable) and addresses only one functionality. 
   3. Keep the number of parameters small.
   4. Ensure that global methods validate all parameters.
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
   4. Follow the same above conventions while naming
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
