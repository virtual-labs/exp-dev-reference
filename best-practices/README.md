## Best Practices for Virtual Labs Experiment Development 

### Introduction
  This document lists the best pratices to be followed while developing a Virtual Lab  experiment.

### General Principles
   It is imperative to
   1. Organize complexity
   1. Maximize clarity and readability of code
   1. Optimize usability and performance
   1. Review early, test frequently
   1. Follow standards and keep the code compliant with latest standards
   1. Use open-source libraries with large communities and active development and support
   1. Use mature tools that are fit for the task at hand
   1. Standardize tools, libraries and coding styles
   1. Build a community, share, discuss, collaborate, contribute
      
### Architecture Style
   1. Make the experiments into static sites, no server-side component
   1. Consult CPE when server-side component is a must
   1. Add dynamic functionality through services

### Performace and Usability
   1. Write code for mobile form-factor and expand it to work on larger screens
   1. Performance should be a fore-thought, not an after-thought
   1. Use light-weight, high performance libraries
   1. Always keep the target audience in mind. Our primary users are from India with<br>
      inconsistent network speeds and low-powered mobile devices
   1. Optimize images for size, minify/uglify code as much as possible
   1. The page load time for an individual page should not exceed 2.0s on a fast-3G network
   1. The size of each page must be less than 5MB
   
### Source Control
   1. Use descriptive commit messages
   1. Commit logically related changes together
   1. Link commits to issues for easier tracking
   1. Tag important milestones
   1. Always keep the master/main branch in deployable condition

### Responsive Design
   1. All Virtual Labs experiments must be responsive and mobile-first.<br>
      Write code for mobile form-factor and expand it to work on larger screens
   1. Use a responsive layout scheme, ideally based on flexbox. Bootstrap has support<br>
      for flexbox from version 4 onward. Bulma is completely based on flexbox
   1. Use responsive versions of elements, e.g. 'table-responsive' css class in place of<br>
      'table' css class
   1. Use responsive images
   1. Design a reasonable column structure for the content. You can reorder the columns<br>
      or stack them so the content makes more sense on different screen sizes
   1. Use flexbox over tables for aligning data so the content stays responsive
   1. Test responsiveness by shrinking the browser window and testing usability
   1. A sample responsive experiment can be accessed [here](https://ssp-iiith.vlabs.ac.in/exp/speech-signal-to-symbol-transformation/)

### General Coding Guidelines
   1. Use descriptive, meaningful, relevant names for files, functions, variables etc
   1. Delete unused, dead, commented code. We have source control to manage change
   1. Properly format the code to make it look clean and readable.
      Avoid big lines. Indent consistently
   1. Keep functions small and focused on a single task.
   1. Refactor repeated code into separate functions so you do not repeat yourself

### General Web-Development Guidelines
   1. Follow the latest standards, HTML5, ES6 and CSS3
   1. Strictly use HTML5 tags. With HTML5, html has moved to completely being a markup<br>
      for explaining the structure of a document(semantic markup vs presentational markup).<br>
      CSS is used for styling. All HTML tags used for styling are 'not recommended' in HTML5
   1. Insert non-critical external JavaScript files at the bottom of the body tag<br>
      and critical external Javascript and external Style Sheets in the head tag<br>
      for better performance
   1. Alternatively, the non-critical Javascript can also be loaded asynchronously so it does<br>
      not interfere with html rendering
   1. Evaluate performance of CDNs for common libraries like Bootstrap, JQuery etc.<br>
      Sometimes downloading them and linking from your own server is faster because<br>
      many CDNs do not have servers in India.
   1. Load non-critcal resources lazily and asynchronously. E.g. A video need not be loaded<br>
      until the user actually plays it
   1. Keep styling separated from content structure
   1. Use open-source, popular libraries over writing own code for css or JS
      
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
   1. Use the the HTML5 doctype in all documents and make sure that the
      <html> element has a  "lang" attribute.  Make sure that the <head>
      at a minimum includes "viewport" and "charset" meta tags.
   1. Use two spaces for indentation in all HTML documents and ensure that there are no
      trailing whitespace. Use HTML5 syntax and use double quotes around attributes.
   1. Use double quotes for attributes
   1. Use meaningful class names
   1. Ensure unique id's for elements
   1. Do not use underscores for classes instead use hyphens
   1. Do not use images for buttons instead use css fonts or bootstrap glyphicons
   1. Use alt attribute for images with proper naming/description for the image
   1. Do not include styles in html as inline or internal css, instead use external
      stylesheets for each feature to make the html and css clean and maintainable.
   1. Prefer SASS(scss) over CSS for properly nested, easy to read code.
   1. Do not use \<br\> for vertical spacing. Use css classes to add padding/margin instead.
      Use \<br\> to show logical separation in content, when required
   1. Do not use special characters ("<", "=" etc.,)
   1. Do not use HTML elements like \<b\>, \<i\> etc, instead use the tags which carry
      some semantics with them, e.g. \<em\>, \<strong\>, \<mark\>, \<cite\>, \<dfn\> etc

### CSS Coding Standards
   1. Use two spaces for indentation in all CSS documents and ensure that there are no
      trailing whitespace. 
   1. Do not declare the css rules on one line 
   1. Align the properties and values with same space
   1. Use shorthand properties wherever possible
   1. When it is not possible to use a library, use browser specific css rules so the
      code works on all browsers (Mainly on firefox and chrome). Always provide
      fallback properties for older browsers.
   1. Do not keep all styles in one large stylesheet, instead create multiple stylesheets
      to reflect the logical organizion of code
   1. Do not use pixels for units, instead use %, em, rem, vw, vh for better responsiveness
   1. Do not repeat yourself. Write a modular code to reuse it
   1. Place all common styles in a seperate stylesheet to reuse it in different templates.
   1. Use media queries at the end of the file
   1. Put spaces before { in rule declarations.
   1. Use hex color codes #000 unless using rgba()
   1. Use double quotes
   1. Try keep all selectors loosely grouped into modules where possible and avoid having
      too many selectors in one declaration to make them easy to override.

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

### Naming Conventions: Files, images, videos etc
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

## Resources and Recomendations
- **Development**
    + **IDE**: VS Code
    + **Code-Formatting**: Prettier
    + **Linting**: ESLint
    + **Code-completion**: Emmet
    + **Local-Server**: live-server
    + **Browsers**: Chrome, Firefox
    + **Unit-testing**: Jest, jsdom
- **Performance**
    + **Performance Testing**: Chrome dev tools<br>
                        [webpagetest](https://webpagetest.org/)
    + **Image compression**: [toolur](https://compressimage.toolur.com/)
- **References**
    + [MDN](https://developer.mozilla.org/)
    + [css-tricks](https://css-tricks.com/)
