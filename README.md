# Bootstrap5 Project
## *Bootstrap is a popular and powerful frontend framework for responsive webdevelopment*<hr>

## Technologies Used:
- Shell and scripting language: Powershell
- IDE: Visual Studio Code  2019
- Frontend: HTML5, CSS, Bootstrap 5
- Version Control: GitHub, GitHub for Desktop

<hr>

## Challenges
- Adding formatting practices not included in tutorial video

<hr>

## Introduction
### *Scope of the Projcect*

*This project will contain introductory information as well as exercises utilizing Bootsrap v5*

### Bootstrap Grids

- Bootstrap utilizes a grid system that supports six responsive breakpoints
- Breakpoints are based on min-width medi queries and effect the breakpoint and all thoase above it
- you can control container and column sizind and behavior by each breakpoint
- Containers center and horizontally pad your content
  - .container will be used for responsive pixel width
  - .container-fluid will be used for 100% will be used for responsive containers
- Rows are wrappers for columns and each column has horizontal padding, or gutters, for space control
- Columns are incredibly flexible and there are 12 template columns available per row
- Gutters are also responsible and customizable; Gutter classes are available across all breakpoints
  - horizontal gutters are changed with .gx-* classes
  -  vertical gutter with .gy-* classes
  -  all gutters are changed with the .g-* classes
  -   .g-0 can be used to remove all gutters
<hr>

### Styling the Landing Page Text

- In order to style the landing page text we must move to the main container under the nav bar container
- our text is placed in the within the main container
- in order to center the text, containers div class will be adjusted like so:
  ```
  <div class="container text-center">
  ```


- We'll then colorize the container by adding a class to the the sub title:
  ```
  <h3 class="text-white">
  ```


- in order to adjust the margins will will edit the div class again like so:
  ```
  <div class="container text center mt-5>
  ```
  - in this instance m stands for margin and t stands for top
  

- Next we will adjust the Main title by adding a class to the header tag to center it, enlarge it, and colorize it
  ```
  <h1 class=text-center display-1>
  ```


- We will now change the font by including a link to our font source above our style sheet
  ```
  <link rel="stylesheet" href="https://use.typekit.net/mhj5wdi.css">
  ```


- Next we will add CSS styling so the html document will accept the font changes
  ```
  .homeText{
    font-family: modesto-open-shadow, sans-serif;
    font-weight: 400;
    font-style: normal;
    color: rgb(195, 255, 0);
  }
  ```

- Finally we will add the homeText class to our Main Title by including the new style class in the header tag:
  ```
  <h1 class="text-center display-1 homeText>
  ```
<hr>

## Grid 1

![Grid One Reference](img/Grid1.png)

#### *During this section we will be building a page with a two column grid*
<hr>

### Things to Remember

- Everything in bootstrap is built upon the grid system, which is a row and twelve columns
  
- each row must take up at least tweleve units, therefore we are building a page with two six-unit columns
  
### Setting up our Code

- First we must create a row div class within our main container
  ```
  <div class="row">
  ```
  - Note about rows: If you're going to have columns, columns must be nested inside of a parent element with a row
  
- A good practice to follow when setting up columns is to scaffold out the basic layout for our columns. This ensures that our divs are closed properly and are structured right.
  
- Another good practice to follow, if you know you're going to have content that will contain  multiple tags, is to wrap a div around the the content within the columns. This allows us to center the content within the column by centering the "wrapper" div. this is done by entering the following code"
  ```
      <main class="flex-shrink-0"> 
       <div class="container">*this is our main container*
        <div class="row">
           <div class="col">
               <div> *wrapper div*
                   COL ONE
               </div> *wrapper div*

           </div> 
           <div class="col">
               <div> *wrapper div*
                   COL TWO
               </div> *wrapper div*
           </div> 
        </div>
       </div> *this is our main container*
    </main>
  ```
  
  
- Set the div class for Col 1 to "bg-dark text light" 
- Set the div class for Col 2 to "bg-secondary text light"
- you can control the gutter by editing the row class
- you can adust paddign by adding p* to the column class
- you can extend the columns all the way down you can set a .minHeight in the CSS style sheet and adding it to the container class
- if you'd like to take mobile viewing into consideration (for bootstrap 4.6 and up) you can add row-cols-* to your class; don't forget you can adjust the gutter with gy, gx, or g
  
<hr>

## Grid 2

![Grid Two Reference](img/Grid2.png)

- Set up column scaffolding, minheight, column background and text, and column height like we did in Grid 1

- use col-* to adjust the size of each column as you see fit, in this instance i used col-3 for the side nav and col-9 for the main content

<hr>

## Grid 3

![Grid Three Reference](img/Grid3.png)

### Setting up the Code

- Set up column scaffolding
- Add comment annotatin left column, right column
- Give the left column a div class of col-7 and give the right column a div class of col-5 
- add two additional divs to the right column and annotate them as right top column and right bottom column like so:
  ```
  <!--RIGHT COLUMN-->
   <div class ="col-5">
    <!--RIGHT TOP COLUMN-->
    <div>

    </div>
    <!--RIGHT BOTTOM COLUMN-->
     <div>

     </div>
    </div>
  </div>   
  ```
  - be sure that your divs are properly closed in order to prevent errors

- Give the left column the class of h-100 so it will stretch to the bottom of the page
<hr>

### Setting up the Right Column

- While the Right Column has a height of 100, we will need to give the top and bottom portion a height of 50, and we will give the bottom column a margin of 2

- Add a button to the bottom right column by entering the following after the first closing div:
  ```
  <div>
    <button class="btn btn-light" type="button">Read More</button>
  </div>
  ```


- Give the the class of "bg-dark text-light border border-top p-2"
- place padding of p-2 in the bottom and top column
  
#### Justifying the stacked boxes

- in order to justiy our boxes, add a flex box class to the right container like so: 
  ```
  <div class="col-5 h-100 d-flex flex-column justify-content-evenly">
  ```

#### Preventing overflow of content

- in order to prevent content overflow, we will need to add the overflow-hidden  class to our right bottom column
<hr>

## Grid 3B


![Grid Three B Reference](img/Grid3B.png)

- Create a new file named Grid3B.html
- Copy and paste the entier contents from Grid 3 to Grid 3B
- Navigate back to the Grid 3 html and create an Unordered list with a nav class within the container div like so:
  ```
  <main class=flex-shrink-0>
    <div class="container h-100 minHeight>    
           <ul class="nav nav-pills mb-1">
               <li class="nav-item">
                   <a href="Grid3.html" class="nav-link active" aria-current="page">Grid 3</a>
               </li>
               <li class="nav-item">
                   <a href="Grid3B.html" class="nav-link" aria-current="page">Grid 3B</a>
               </li>
           </ul>
  ```

- Copy the unordered list to the Grid 3B html file
- remove the button, as we will not need it
- remove the flex column and overflow from teh right column div
- create a form tag and give it a class of "d-flex"
- create an input tag and give it a class of "form-control me-2" give it a type and placeholder of search, and give the tag a aria-label of search.
- Add a button and give it a class of "btn btn-outline-light" give it a type of submit and a label of search
  ```
  <button class="btn btn-outline-light" type="submit">search</button>
  ```

- Remove the height and overflow from the right bottom column, give the title a h5 title of More Articles and create another navigation using the unordered list
- the ul will have a class of "nav flx-column"
- create an ordered list witha  class of "nav-item
<hr>

## Note
- For the sake of brevity, the remaining grid instructions will be provided upon request. - J. Bright

### Project References

- <a href="https://learn.coderfoundry.com">Coder Foundry Complete .Net Coding Bootcamp</a>
- <a href="https://getbootstrap.com/docs/5.0/getting-started/introduction/">Bootstrap 5 Docs</a>
- <a href="https://getbootstrap.com/docs/5.0/utilities/colors/">Bootstrap 5 Colors</a>
