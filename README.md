# coursera-test
For Coursera Class (https://github.com/jhu-ep-coursera/fullstack-course4) 

## Links ##
* GH Pages: http://rmavery.github.io/coursera-test/
* CSS Zengarden: http://www.csszengarden.com 

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

## Character Entity References
* Characters that always need to be escaped
-- &lt; 
-- &gt; 
-- &amp; 
* Other Entity references 
-- & copy ; = &copy; 
-- & nbsp ; = &nbsp; 
-- & quot ; = &quot; 
* Do not use the nbsp for additional spaces.   
-- Wrap in a span tag and then apply margin to move it further from the other word. 

## Creating Links
* Link is an 'a' element with a value of 'href' 
* Browser will assume file is in same directory unless directory information is provided
* You should always provide a 'title' attribute for visually impaired users 
* You can put a &lt;div&gt; inside an 'a' tag because an 'a' tag is both an inline and a block level element
* External link points to a resource not within your site (usually hosted on a different domain name than your web) 
* _target attribute lets you determine if you want to open the tab in your window _self or another window _blank 
* A Fragment identifier is a href=# with a pound sign in front of the identifier.  
-- You can use &lt;section ="sectionName"&gt; to identify the fragment
-- You can create another anchor &lt;a name="sectionName" &gt; 
* If you have a fragment identifier in your URL, you can send that URL to a friend which will take them right to that section. 
* They have become more important because they are used to identify markers in a SPA (Single Page Application) 

## Displaying Images
* Using the &lt;img tag
* Add a 'src=' with a pointer to the file
* The %lt;img tag is an 'inline' element
* Images are used as a visual anchor in your page.  
* Use the 'witdh=' and 'height=' tags so the page knows how to set aside the space for the images before it's loaded.  
* You can use the Chrome Tools 'Network (Throttling)' to demonstrate a slow internet connection. 
* Also, if you have a broken image the visual spacing will still be correct if you put the size


## Power of CSS
Users absorb and relate to content by the experience of how they consumed it.  Structure alone, for that reason is not enough. 
* CSS is an incredibly powerful technology
* User experience of content matters

## Anatomy of a CSS Rule 
* Selector (p) followed by open and close curly braces
* The whole selector{} is called a 'Declaration'
* Inside the braces, is a 'Property' and a 'Value' 
* Separated by a Colon, and followed by a Semi-Colon
* Zero or more declarations is allowed
* Collection of rules is called a 'StyleSheet' 

## Element, Class, and ID Selectors
* Javascript libraries use the browser select API to attach behavior and data to elements in much the same way as CSS attaches style to those selectors. 
* Element Selector (selects elements, e.g, &lt;p&gt;) 
* Class Selector (begins with a . and then the name of the class) 
* ID Selector (begins with a # and the name of the ID) (ID must be unique on the page) (case sensitive)
* Grouping Selector (div, .blue{ color:blue;} will affect any div tag, AND any class="blue") 

## Combining Selectors
* Element with class selector p.big (Element &lt;p class="big" &gt;) 
* Direct Child selector (Selector followed by article &gt; p ) (Any &lt;p&gt; directly following the the &lt;article&gt;) 
* Descendent Selector (SelectorA [sp] SelectorB) every descendent SelectorB (not only direct child) of SelectorA
* You can assign multiple classes to a single element by listing with a space between them. 
* .highlight.mainpoint requires that the element has both classes 'highlight' and 'mainpoint' assigned to it.  
* Also Lookup... 
* -- Adjacent Sibling Selector
* -- General Sibling Selector

## Pseudo-Class Selectors
Style based on user interaction with an element
* Selector:pseudo-class name, e.g, {:link, :visited, :hover, :active., nth-child(...)} 
* Style unordered list as a menu
* -- list-syle: none; 
* -- text-decoration: none;
* -- background-color:green;
* -- border: 1px solid blue; 
* -- color: black;
* -- display: block; (will try to fill up the line) 
* -- text-align: center; 
* -- width:200px;
* -- margin-bottom: 1px; 
* a:hover, a:active {background-color:red; color:purple; } 
* header li:nth-child(3){ will affect the third child LI} 
* section div:nth-child(odd){modifies every other div)
* section div:nth-child(4):hover{background-color:green; cursor:pointer;) 
* Make sure your selector is still readable or you'll end up with a maintenance nightmare

 




:relieved:
:confused:
