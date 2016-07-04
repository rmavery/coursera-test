# Module 3

## Visit the Client 
* Most clients have no idea what they want
* It's your job to ask questions 
* Bring web site examples
* They will want A LOT of information on the site
* When everything is important, nothing is important
* Encourage client not to cram information on the website
* Find a way for the client to invest in the project 
* Client needs to feel like they have some skin in the game.  
* Have them commit to pay for product photography or something along those lines 
* Designate one person responsible for decisions
* Limit the number of revisions up front (if free) 
* For paying, limit the number of 'Free' revisions 
* Google 'web development client questionnair' 
* Involve others if needed 
* Contact a local college and see if a graphic student wants to join you and add content for their resume
  * Same for photography
* 

## Design Overview 
* Balsamiq Mockups 3 - https://balsamiq.com  $89.00
  * Mockup files are actually text based, so you can check them into a repository and keep diffs 
* Big picture when you first enter the page is called a 'Jumbotron' 
* Main stuff users want to see when they go to a site
* When you go to a 'Mobile' page, convert menu to a hamburger
* On mobile, put phone number front in dominant place to make it easy for users to get to. 

* From Designers
  * Color Scheme 
  * Photography
  * Fonts - Stick with Google Fonts for free fonts 
  * Professional Web Designers usually use Adobe Photoshop to design a web page 
  * 
  
* Fonts 
* http://www.w3schools.com/cssref/css_websafe_fonts.asp
* https://www.google.com/fonts
* Paste the 'font' link in your 'head' section where you put the css stuff. 

  
## Coding Basics of Navbar Header 
  * When you use 'BrowserSync' if you want to address all files and folders and everything inside the folders, you must use "**/*"
  * Bootstrap will give you a 'Base' class, i.e., 'Navbar' and a subclass, i.e., 'navbar-default' 
  * Look up the 'navbar-header' class.  It's specific and helpful, but requires that it be in a specific place.  
    * https://www.getbootstrap.com/components/#navbar 
  * Look up 'navbar-brand' class 
  * Class 'pull-left' is basically 'float-left' 
  * If you want elements to disappear on certain screen sizes, you can use the class 'visible-md' and 'visible-lg' 


## Coding Button for Future Collapsable Menu
* Take care of the 'mobile' view first.  The Hamburger view.  
* The 'Navbar' Collapsed Class does not exist in the Bootstrap CSS.   This is done through .js in boostrap.js
* class 'sr-only' is for 'Screen Reader' only. 
* This has to be programmed using JavaScript, but Bootstrap has this programmed out of the box

## Coding Nav Manu Buttons 
* The 'button' has the 'data-target="#collapsable-nav"' which JS uses to identify the target 'id="collapsable-nav"' in the second div below.  
* The div id="collapsable-nav" contains the content that should be made invisible unless the toggle button is clicked.  
* The div id="collapsable-nav" has required classes 'collapse' and 'navbar-collapse' 
```
<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target=#collapsable-nav" aria-expanded="false"> 
 <span class="sr-only">Toggle Navigation</span>
 <span class="icon-bar"></span>
 <span class="icon-bar"></span>
 <span class="icon-bar"></span>
</button> 

<div id="collapsable-nav" class="collapse navbar-collapse">
 <ul id="nav-list" class="nav navbar-nav navbar-right">
  <li>
  </li>
 </ul> 
</div> 
```
* Media Queries
```
/****************** Large devices Only **************/
@media (min-width: 1200px) {
}
/****************** Medium devices Only **************/
@media (min-width: 992px) and (max-width: 1199px){
}
/****************** Small devices Only **************/
@media (min-width: 768px) and (max-width: 1199px){
}
/****************** Extra Small devices Only **************/
@media (max-width: 767px){
}
```
* Font Size (vw) = Viewport Width
  * 1vw = 1% of viewport width
 
##Coding the Jumbotron 
```
<div id="main-content" class="container">
 <div class="Jumbotron">
 <img src="images/jumbotron.jpg" class="img-responsive visible-xs">
 </div>
</div>
```
* You can't easily stretch and contract the image when the screen size changes in the 'jumbotron' if you are using a 'Background Image'.   
* Recommend using an '<img' tag for the smallest with the class 'img-responsive'. Then set different image sizes in the different @media queries using the background image 
* Position: Relative will set up an 'anchor' for all child elements contained within that element.  

## Coding the Footer


