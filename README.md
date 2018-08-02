# Intro to Sass

### LEARNING OBJECTIVES
*After this lesson, you will be able to:*

- Have a clear understanding of what Sass is and the benefits of writing in Sass.
- Will be able to develop a clean css workflow in Sass. 


### STUDENT PRE-WORK
*Before this lesson, you should already be able to:*

- Can write and understand clear CSS.
- Understand how variables and nesting works.  
- Can use cmd line to initialize and compile projects.

## Overview

#### What is Sass? 

Sass is an extension of CSS that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized, and get small stylesheets up and running quickly, particularly with the help of the Compass style library.

As you can see Sass can add alot of functionality to css to improve front end development life.

##### So let's get Sassy! 
<img src="https://media.giphy.com/media/BhhvMflNABkoE/giphy.gif" width="300px">

## Common Myths

There are alot of common misconseptions about Sass so let's debunk those. 

- Sass will change the way I write css entirely.

Sass is no different then standard css in 90% on its syntax. In fact Sass has devoted to be compatible with ALL versions of css. 

Here is standard css.

``` css 
    Article{ font-family: helvetica; }
    h1{ color: #333377;}
    p{ color: #333377;}
    P:hover{ color: #cc3333;}

```
And here is Sass.
```scss 
    $main: #333377;
    
    Article{
        font-family: helvetica;
        h1{ color: $main;}
        p{ color: $main;
        &:hover{ color: #cc3333;}
        }  
    }
    
```

## Installation

Sass can be installed globally via homebrew! 