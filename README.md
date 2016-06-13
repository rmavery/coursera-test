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
* <div> is generic block element (new line before and after this tag)
* <span> generic inline element 
* https://www.w3.org/TR/html5/dom.html#kinds-of-content shows all content types. 

## Heading Elements 
### Semantic HTML element
* Implies some meaning to content 
* May help SEO
### Headings <hx>
* Although these do render with visual distinction, you should not use for visual styling 
* Heading tags convey the central topic of the content


## Semantic Elements (Inherently convey some meaning) 
These don't really provide any additional formatting, but they're block level tags, and give approximately the same functionality as a <div> or a <span> tag.  
### <Header> tag 
* Header information about the page
* Navigation
* Company Logo
### %gt;Section&lt; Tag
* May contains <Article> elements 
* <Article> could have a <Section> tag within it 
### <Aside> Tag 
* Content indirectly related to the main content of the page 
### <Footer> Tag 
* 


:relieved:
