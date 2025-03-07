Use @for to Create a Sass Loop


The @for directive adds styles in a loop, very similar to a for loop in JavaScript.

@for is used in two ways: "start through end" or "start to end". The main difference is that the "start to end" excludes the end number as part of the count, and "start through end" includes the end number as part of the count.

Here's a start through end example:

    @for $i from 1 through 12 {
      .col-#{$i} { width: 100%/12 * $i; }
    }
The #{$i} part is the syntax to combine a variable (i) with text to make a string. When the Sass file is converted to CSS, it looks like this:

    .col-1 {
      width: 8.33333%;
    }
    
    .col-2 {
      width: 16.66667%;
    }
    
    ...
    
    .col-12 {
      width: 100%;
    }
This is a powerful way to create a grid layout. Now you have twelve options for column widths available as CSS classes.

Write a @for directive that takes a variable $j that goes from 1 to 6.

It should create 5 classes called .text-1 to .text-5 where each has a font-size set to 15px multiplied by the index.
