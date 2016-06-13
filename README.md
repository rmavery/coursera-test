# coursera-test
For Coursera Class (https://github.com/jhu-ep-coursera/fullstack-course4) 

## Links ##
* GH Pages: http://rmavery.github.io/coursera-test/

* Standard: 
* Can I Use: https://caniuse.com
 -- Tells you which browser supports what
* Validator: https://validator.w3.org
* W3C Schools: http://www.w3schools.com/browsers/browsers_stats.asp
* Search Engine: http://www.google.com 
* 
 
## Git Commands ##
* Git Clone https://github.com/rmavery/coursera-test.git
* Git remote add origin https://github.com/rmavery/coursera-test.git
* Git Pull

## Browser Sync Commands ##
Apparently this needs to be run in NodeJS command window (maybe not on MAC) 
* Browser Sync Command: browser-sync start --server --directory --files "*"

## Content Models
### Block Level Elements
* Render to begin on a new line (by default) 
* May contain inline or other blocklevel elements within them. 
* Rougly translate into HTML5 category of 'Flow Content' 

### Inline Elements
* Renders on the same line (by default)
* May only contain other inline elements 
* Roughly translate to HTML5 category of 'Phrasing Content' 

### HTML5 Replaces definitions of elements
Examples: div-and-span.html 
* <div&gt; is generic block element (new line before and after this tag)
* <span&gt; generic inline element 
* https://www.w3.org/TR/html5/dom.html#kinds-of-content shows all content types. 

## Heading Elements 
### Semantic HTML element
* Implies some meaning to content 
* May help SEO
### Headings <Hx&gt;
* Although these do render with visual distinction, you should not use for visual styling 
* Heading tags convey the central topic of the content


## Semantic Elements (Inherently convey some meaning) 
These don't really provide any additional formatting, but they're block level tags, and give approximately the same functionality as a &lt;div&gt; or a &lt;span&gt; tag.  
### &lt;Header&gt; tag 
* Header information about the page
* Navigation
* Company Logo
### &lt;Section&gt; Tag
* May contains &lt;Article&gt; elements 
* &lt;Article&gt; could have a &lt;Section&gt; tag within it 
### &lt;Aside&gt; Tag 
* Content indirectly related to the main content of the page 
### &lt;Footer&gt; Tag 
* 

## HTML Lists 
* The only thing allowed inside a &lt;UL&gt; or &lt;OL&gt; tag is an &lt;LI&gt; tag.  
* &lt;UL&gt; created a bulleted list
* &lt;OL&gt; creates a numbered list

 


:relieved:
