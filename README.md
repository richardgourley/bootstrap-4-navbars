# Bootstrap 4 Navbars

## Build a bootstrap navbar step by step

It proved tricky to get the bootstrap navbar I required set up exactly as I wanted it for a project.  I thought I'd show the step by step process I used in creating a unique navbar with bespoke styling.

Using basic-navbar.html as a starting point, each example in numbered order, builds upon the previous example to build up to the finished navbar in example11.html

Step by step
1. Move brand and menu inside container div with margin
2. Keep brand left but menu to the right of div container.
3. Add logo - make sure it sits nicely in the navbar and has the correct width.
4. Add text to right of logo - make it stand out with uppercase and bold font weight.
5. Add sticky top - make it stay at the top when the user scrolls down.
6. Change nav background to dark blue
7. Change nav brand text color and change links brand text color to a light yellow.
8. Change color of links when we hover over menu links to a dark yellow.
9. Modify the background color of the collapsable menu for smaller devices and ensure grey lines of toggler icon still appear correctly.
10. Change dropdown menu links color to a more readable color.
11. Add border and shadow to bottom of navbar

The process goes from example1.html through to a completed bespoke navbar in example11.html. 
The end result has completely bespoke color scheme - and doesn't rely on bootstrap navbar-light and navbar-dark classes. 
The inital base-navbar.html file starts with a basic bootstrap navbar with branding text and a dropdown menu on the left that collapses on mobile devices... 

NOTE: The inclusion of css in <style> is only for demonstration purposes. For any devs reading this, it's always best practice to include css in its own file and call it.  NOTE! Bespoke css has to be called AFTER the bootstrap styles are loaded.
The bootstrap JS files are included for demonstration purposes as well. Again, its better to separate them into their own files and call them via <script src="..... 

=====================================

### 1. Example1 - FROM basic-navbar.html
- I wanted all navbar elements to have margins and NOT have a full width container. However, I wanted the navbar itself to be full width so I only put the brand name and menu inside the div with class container. 
- ACTION: Placed brand name and menu items inside a bootstrap <div class="container"... (bootstrap built in class)

### 2. Example2 - FROM example1.html
- I wanted to keep the brand name on the left but I didn't want the menu to appear next to it.  I wanted the menu to appear on the right of the navbar.
- ACTION: I added the class name 'justify-content-end' to the menu links div = <div class="collapse navbar-collapse justify-content-end"

### 3. Example3 - FROM example2.html
- I wanted to add in a logo that fits nicely in the navbar.  After experimenting with sizes, it seems that setting width to 80 works well with bootstrap navbars.
- ACTION: Added logo <img> within <a class="navbar-brand"> tag.  Aligned it in the center to make sure it sat nicely and also set the width to 70, all with built in bootstrap classes.  Added a right margin level 2 class (mr-2) to leave a little space between the image and the company name/ slogan.

### 4. Example4 - FROM example3.html
- I wanted to make the text to the right of the logo stand out and look more professional.
- ACTION: Placed the company name inside a <span> tag below the image but still inside the <a> brand tag.  Added the built in classes - text-uppercase, font-weight-bold, and text-light to the <span> element.

### 5. Example5 - FROM example4.html
- I wanted to make the navbar sticky so that stays at the top of the screen whenever the user scrolls down the page.
- ACTION: In the <nav> tag, I added the class 'sticky-top'.

### NAVBAR SCHEME

### 6. Example6 - FROM example5.html
- Now, I wanted to start adding my own bespoke color scheme. Firstly, I wanted to change the navbar to a bespoke dark blue color.
- ACTION: Firstly, added bespoke styling to the navbar class. Secondly, in order for our own scheme to work, I had to remove the default classes from the <nav> tag - navbar-light and bg-light. (These classes automatically take care of adding dark text to a light background - if that works for your navbar, I would keep that in there as it takes care of link hovering and the collapsible button styling for mobile devices.  Use steps 6 onwards when you need completely bespoke colors for your navbar.)

### 7. Example7 - FROM example6.html
- I wanted to change the brand name text and the menu links to a light yellow color to go on top of the dark blue background.
- ACTION: Add and modify navbar a{} in our own styles. (Must load AFTER bootstrap css loads when you are adding into a stylesheet)

### 8. Example8 - FROM example7.html
- Here, I wanted to make the links a darker yellow when we hover over them.
- ACTION: Add and modify .navbar a:hover{} to our darker yellow color.

### 9. Example9 - FROM example8.html
- I wanted to have the menu icon for the collapsed menu on smaller screens to have the same color border and the same color bars as the menu links.
- Using the bootstrap classes navbar-dark/light with bg-dark/light automatically gives a darker or lighter version of the collapsed menu. However, if you need bespoke colors, the following action works...
- ACTION: 
  - Firstly, I included the stylesheet for Font Awesome to use customizable icons.
  - Secondly, I replaced the class 'navbar-toggler-icon' in the <span> tag located in the <button> tag with an icon class called 'fa fa-bars'.
  - Thirdly, I changed the border color of the outer button class 'navbar-toggler' to the same yellow color as the menu links.
  - Finally, I added and modified the class 'fa-bars' to the yellow color.  This ensured the border and the menu bars in our collapsed menu button were the same as our links.
    (NOTE: You can use any icon for your menu that you prefer.  I used font awesome in this project because their icons allow you to change colors without breaking or needing to modify other bootstrap classes.)

### 10. Example10 - FROM example9.html
- Here, because all links are set to yellow, we needed to change the color of the links on the dropdown menu to a readable color for a white background.
- ACTION: I added and modified .navbar a.dropdown-item{} to color:grey.

### 11. Example11 - FROM example10.html
- Finally, we want to add a little bit of shadow and a border to the bottom of the navbar.
- ACTION: To set shadow we can use the built in bootstrap 'shadow' class so we add that to the <nav> tag.
I then added a border-button setting to the .navbar{} stylings already in use for our navbar background color.

The result of this is a unique navbar and toggle button for smaller screens, built with some personalized styling but also using bootstrap classes where relevant.

