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

## Style Placement
* Inline Styling - Added directly to the tags (Least reusable, Least Preferred)
* In head tag - not helpful for other pages
* External style sheet - Most reusable, preferred
* -- Just styles on a sheet, doesn't require any specific wrapping to identify the page as a CSS
* In a real world website, you almost always want your styles outside of your sheet. 
* Head styles are most often just used to override external styles

## Conflict Resolution
Cascading is an algorithm defining how to combine properties values from different sources.  (Using a cascade algorithm) 
* Origin, Merge, Inheritence, Specificity
* Origin precedence rule (Last Declaration Wins).  
* -- HTML is processed top to bottom.  The lower on the page, the more precedence it has. 
* Merge is when two selectors are attributed to a single element, but different attributes
* -- When no conflict, e.g, Font-Size and Color, they will merge
* Inheritance - DOM Tree
* Body >> Element >> Element -- All children of a body tag
```
 body {
 color: red;
 text-align: center; 
 font-family: Helvetica;
 }
 ```
*  p { color: blue;} (body attributes will be hit unless it's a P element
* Specificity - Most specific selector wins
* Style = "...", ID, Class, Pseudo-class, Attribute, # of Element
* 1.) Style (1000 points each)
* 2.) ID    (100 points each) 
* 3.) Class, Pseudo-class, Attribute  (10 points each) 
* 4.) # of Element  (1 point each) 

| Style | ID | Class, etc. | # Element | 
|----------|----------|----------|---------|
| 1000 | 100 | 10 | 1 | 

* Count the number of instances of each, and put them in left to right order as 'Style', 'ID', 'Class, etc', # of Element
* Total the number of each, and then that results in a number.  Highest score wins
* !important is worth a bazillion points, because it overrides everything else. 
* While it's tempting to use !important, but it's a code smell, and will be a maintenance nightmare

## Styling Text
* http://www.w3schools.com/cssref/css_websafe_fonts.asp
* 
```
<style>
.style { 
  font-family: Arial, Helvetica, sans-serif;
  color: #0000ff;
  font-style: italic; 
  font-weight: bold;
  font-size: 24px; /* Default would usually be 16px */ 
  text-transform: capitalize; 
  text-align: right; 
 </style> 
 ```
 
 * Relative Font Sizing
```
<style>
body { 
 font-size: 120%;
}
</style>
```
* em is a unit of measurement equivalent to the letter M in the text.  
* 2em wuold be a font twice the size of the rest of the text.  
* Relative font-sizes don't have an 'overriding' effect, but rather a cumulative effect

``` 
<div>Regular Text</div>
<div style="font-size: 2em;">2em text
  <div style="font-size: 2em;">4em text (2em * 2em)
    <div style="font-size: .5em;">2em again! (1/2 the size)</div>
  </div>
</div>
```
* When a user increases the zoom, relative sizes will increase together. 


## The Box Model
* Each box consists of padding, border, margin, width, height, content
```
<style>
body { 
  background-color: gray;
  }
  #box {
   background-color: blue; 
   padding: 10px 10px 10px 10px; /* Top, Right, Bottom, Left */ 
   border: 5px solid black; 
   margini: 40px; 
   width: 300px; 
  } 
  /* The above box will be 300 + 10px + 10px + 5px + 5px.  minimum wide.  You are actually setting the 'width' of the content */ 
  #content {
    background-color: #90EE90; //Green
  }
</style>
<div id="box"> 
  <div id="content"> Lorem Ipsum dolor sit amet, consectetur adipisicing elit.</div>
</div> 
```
* If you look at this page, you'll see 8px of gray around the box.  If you examine the element, you'll see that it's coming from the 'user agent stylesheet' (which is the browser itself) 
* To reset ... 
``` 
body { 
 margin: 0; 
 padding: 0; 
}

```
* CSS3 has
``` box-sizing: border-box; (vs content box) which ensures the box size is the width/height ``` 
* box-sizing  is not an inherited property.  
* You can however use the * selector 
```
* { 
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  }
  ``` 
  Will apply box-sizing: border-box to every element 
  ### Cumulative Margins 
  * If you have a 40px on the right box, and 50px on the right, you'll have a 90px 
  * Top and bottom however, will collapse, and the larger margin will win
  
*Look up the Emmit plugin* 
* Dealing with 'Overflow' - by default, the overflow is visible.  You can make it 'hidden', 'auto'
* Users absolutely hate double scrolling except for things like long legal documents, e.g, terms of service
* 

## Background Property
```
#bg{
 width: 500px;
 height: 500px;
 background-color: blue; 
 background-image: url("relative_to_css.jpg"); 
 background-position: top right;
}
```

## Position Elements by Floating
* Most designs today are done by floating
* When you float an element, the browser takes them out of the regular document flow
* For Floated elements, the margin on the top never collapses
* To make sure you resume the document properties, you can use the 'clear' attribute. 
* When floated elements can't fit on the same line, they get pushed to the next line 


## Relative and Absolute Element Positioning
* Static positioning is the default document flow
* Relative positioning is relative to it's position on the normal document flow
* Relative positioioning DOES NOT take it out of the normal document flow.   
* If the element is moved, the DOM still preserves the previous location of the element
* You can also use negative values for the offset

* *Absolute* 
* All offsets (top, bottom, left, right) are relative to the position of the nearest anchor which has positioning set on it, other than static. 
* By Default HTML is the only element that has non-static positioning set on it (relative) 
* Element is taken out of normal document flow 
* Absolute will be taken out of the document flow
* If you have a container element that is offset, then anything inside of it is offset right along with it if relative

## Media Queries 
* sets styles based on the media on which the web page is being displayed 
* Media queries start with @media, and are followed by a media feature, and contains the styles
* If the media-query (feature) resolves to 'TRUE' then the styles will be in effect 
* Most common is (max-width) and (min-width) 
* You can also use logical operators, e.g, @media (min-width: 768px) and (max-width: 991px) {...}
* A comma between two queries, is seen as an 'or' operator. 
* It's common to have some base styles, and then only modify base styles on different screen sizes
* DO NOT overlap range boundaries (break points) in your media queries
```
@media (max-width: 767px) {
  p{
     color: blue; 
   } 
 } 
```
* Standard width ranges are in the twitter bootstrap documentation

## Responsive Design
* Beginning around 2013, browsing on a mobile device outnumbers browsing on a desktop or laptop
* Site designed to adapt it's layout to the viewing environment by using fluid, proportion-based grids, flexible images, and CSS3 media queries 
* Content is like water.   The content should become the container.  
* Sites layout adapts to the size of the device
* Content verbosity or it's visual delivery may change 
* Alternatives, are a server side agent that detects what kind of device it is, and then serves up different web sites based on the type of device. 
* Most common responsive layout is a 12-column grid 
* 12 is used because it's easily divisible by 2,3,4,6 and 12
* 1 column is 1/12 or 8.33% 
* You can also nest a 12 column grid within your grids
* You have to tell the browser that your website is 'Responsive' (using the 'Viewport' metatag) 
```<meta name="viewport" content="width=device-width, initial-scale=1">``` 


## Introduction to Twitter Bootstrap 
* HTML, CSS, and Javascript Framework for developing responsive mobile first projects 
* CSS needs to target a particular CSS structure
* Javascript Framework based on JQuery 
* Mobile First Framework 
  * Content first 
  * Plan for mobile, but you CAN plan for desktop first if it makes you more comfortable 
  * Plan for mobile from the start 
 * Complaints
   * To big and bloated
   * You can write your own that's more targeted and smaller
 
## Bootstrap Grid System 
* Grid REQUIRES that it be inside a 'container' or 'container-fluid' class. 
* The 'row' class creates a negative margin to counteract the padding that the 'container' sets up.   
  * This ensures that the left margin of content will align because the container will have margin padding.  It just makes things look slightly off. 
* Column class = 'col-SIZE-SPAN' 
  * Size = Screen width range identifier, sm = small, md = medium, lg = large
  * Span = How many columns the value should span. 
  * If your screen width goes below a particular screen size the column spans will collapse (stack on top of each other) 
  * An element that pushes the total columns over 12 will automatically wrap to the next line
  * 
``` 
<header class="container">
   <nav class="row"> 
       <div class="col-md-4">Col 1</div> 
   </nav> 
</header> 
```
* If you add 'col-md and col-sm in the same tag, you can have different column widths for different screen widths
* All Columns must be inside a 'row' class
* If no other rules apply, xs will ALWAYS keep the same layout no matter what size screen. 
``` 
<div class ="container-fluid">
   <div class="row"> 
       <div class="col-md-4 col-sm-6">Col 1</div> 
       <div class="col-md-4 col-sm-6">Col 2</div>
       <div class="col-md-4 col-sm-6">Col 3</div>
   </div> 
</div> 
```
  



:relieved:
:confused:
