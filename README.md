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

There are alot of common misconseptions about Sass but let us tackle the biggest ones.

- Sass will change the way I write css entirely
- Sass is messy code.
- Sass will make my site less compatible across browsers.

### The Truth

Sass is no different then standard css in 90% of its syntax. In fact Sass has devoted to be compatible with ALL versions of css. 

Here is standard css.

``` css 
    Article{ font-family: helvetica; }
    Article h1{ color: #333377;}
    Article p{ color: #333377;}
    Article p:hover{ color: #cc3333;}

```
And here is Sass.
```scss 
    $mainColor: #333377;
    
    Article{
        font-family: helvetica;
        h1{ color: $mainColor;}
        p{ color: $mainColor;
        &:hover{ color: #cc3333;}
        }  
    }
    
```
As you can see Sass reads the same as standard css but instead of calling each parent container you can nest the children elements inside the css! So much cleaner to read alrady. 

Did you also notice the amazing $ symbol? We were able to save that color as a variable to call in our properties. This means we can from one location update multiple css elements! This is only a few of the way that Sass can help you step up your css game.

## How does Sass work?

Sass takes your written Scss file and compiles it into css to be used in your site. There are a couple ways to do this, but we will be showing you the simplest way in terminal. 

### Installation

Sass can be installed globally via homebrew! 


#### In terminal run
```bash
$ brew install sass/sass/sass
```

This will allow us to run the Sass commands to compile the Sass into regular Css. You'll need to tell Sass which file to build from, and where to output CSS to. For example, running

 ```bash 
 sass input.scss output.css 
 ``` 
 
 will take a single Sass file, input.scss, and compile that file to output.css.

You can also watch individual files or directories with the --watch flag. The watch flag tells Sass to watch your source files for changes, and re-compile CSS each time you save your Sass. If you wanted to watch (instead of manually build) your input.scss file, you'd just add the watch flag to your command, like so:

```bash
sass --watch input.scss output.css
```