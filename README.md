# Front-End-Developer-guidelines
Front End Developer's Basic Guidelines

## Table of Contents
  - [HTML](#html)
  - [CSS](#css)
  - [Javascript](#javascript)
  - [Cross Browser Compatible](#cross-browser-compatible)
  - [IE 8](#ie-8)
  - [Code Standards](#code-standards)

## HTML
1) Doctype
   ```
   <!DOCTYPE html>
   ```
   The  ```<!DOCTYPE> ``` is not an HTML tag, it lets the web browser know the HTML version in the web page. It is the first thing in the HTML file.

2）Favorite HTML5 Feature
    - Audio and Video
    - Section
    - Heeader and Footer
    - Nav

## CSS
1) Specificity  
   Style attribute from most to least：
   ```
   specific (inline style) > ID > Class [pseudo-class, attribute] > Elements
   ```
   pseudo-class:
   ```  
   a:link, a:visited
   ```
   pseudo-element selector: 
   ```
   div:first-letter, div:before
   ```
  
2) Cascade
   
   - Importance
   ```
   <div class="movie" id="starwars">Star Wars</div>
   ```
   ```
   #starwars {
     border: 1px solid #000000;
   }
   .movie {
     border: none !important;
   }
   ```
   Note: Do not recommend
   - Specificity
   
   - Source order
   ```
   p {
      color: #000000;
   }
   p {
      color: #cccccc;
   }
   ```
3) Box Model: content, padding, border, and margin
   - Content: The text or image content of the box
   - Padding: an area around the content
   - Border: A border that goes around the padding and content
   - Margin: an area outside the border
   
   Note: The padding and margin are transparent
   
4) Display
   ```
   display: inline;
   ```
   The elements like ```<span>```, ```<em>```, or ```<b>```. 
   margin-top, margin-bottom, padding-top, padding-bottom, width, and heigh will not work.
   ```
   display: inline-block;
   ```
   margin-top, margin-bottom, padding-top, padding-bottom, width, and heigh will be respected.
   
 5）Favorite CSS3 Feature
    - Webfonts
    - Media Query
    - Multile Backgrounds
    - Box Shadows
   
## Javascript
1) Scope: Local and Global
2) Asynchronous JavaScript And XML (AJAX): is a way to communicate to the server without reloading the page. It uses ```XMLHttpRequest``` to communicate to a server-side script to retrieve data formatted in JSON, XML, HTML, or plain text. 
   - Advantages
     
     a) Reduce the traffic travels between the client and the server
     
     b) Increases performance and speed with faster response time
     
   - Disadvantages
     
     a) Increase design and development time
3) Basic Knowlege: use for widgets
   - Dropdown
     ```
     function myFunction() {
         document.getElementById("myDropdown").classList.toggle("show");
     }
     ```
     ```classList```: returns the class name(s) of an element, it is useful to add, remove and toggle CSS classes on an element.

     ```toggle```: between hiding and showing an element.

   - Tab
     ```
     event.currentTarget.className += " active";
     ```   
     ```   
     <body onclick="targetFunction(event)">

        <p>current target</p>

        <p><strong>Note:</strong> only target</p>
     </body>
     ```   
     ```currentTarget```: returns the element whose event listeners triggered the event, even though it is useful during capturing and bubbling. In the example above, it will only return body, even though you click ``` <p>``` or ```<strong>```  tag.

     ```target```: returns the element that triggered the event. In the example above, it will return the event you triggered.
   - Accordions  
   ```nextElementSibling```: returns the element immediately following the specified element

## Cross Browser Compatible
1) Prefix CSS styles
   ```
   -moz- /* Firefox and other browsers using Mozilla's browser engine */
   -webkit- /* Safari, Chrome and browsers using the Webkit engine */
   -o- /* Opera */
   -ms- /* Internet Explorer (but not always) */
   ```

2) Reset - use [normalize.css](http://necolas.github.io/normalize.css/) 
 
3) Clear floats
   ```
   .clearfix:after { 
      content: "."; 
      visibility: hidden; 
      display: block; 
      height: 0; 
      clear: both;
   }
   ```
   
4) Box Model - avoid padding with widths
   ```
   * { 
      -webkit-box-sizing: border-box; /* Safari/Chrome, other WebKit */
      -moz-box-sizing: border-box; /* Firefox, other Gecko */
      box-sizing: border-box; 
   }
   ```
 
 
 
## IE 8 
    
1) HTML
   - Some of the new elements that HTML5 includes that IE8 doesn’t support
   ```
   section, article, nav, header, footer, aside, and canvas
   ```
   ```
      header, section, footer, aside, nav, main, article, figure {
      display: block; 
   }
   ```
       
2) CSS
   - No media queries
   - No keyframes
   - Do not support transform or transition
   - No nth-of-type or nth-child selectors
   - Bootstrap do not support IE8
       
3) Javascript
   - Angular, React – none of the most recent versions of any of these support IE8
 
## Code Standards
1) Progressive Enhancement
2) Team members keep consistency and conventions
3) Solutions should be as simple and clear as possible
4) Readable code is critical
5) Avoid in-line styles and in-line JavaScript whenever possible
