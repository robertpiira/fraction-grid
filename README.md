fraction/grid
=============

A Fluid grid system based on SCSS.

Demo at: <http://piira.se/projects/fraction-grid>

The basics
----------

Fraction grid uses `display: inline-block;` for stacking columns horizontally.

The column gutters are created with the help of `box-sizing: border-box;`.

On top of this, Fraction grid runs on SCSS (SASS) for a semantic markup and a cleaner and more maintainable CSS workflow.

The how
-------

The index.html and fraction-demo.scss provide a basic structure and examples of how Fraction grid can be used.

The thinking
------------

As the name "Fraction grid" implies, the way column widths are calculated are pretty "fractional". The way this works is that each individual layout unit includes a SASS mixin called `grid-unit`, this mixin also takes a couple of parameters,

1. How many columns/parts should this unit span.
2. What is the total number of columns/parts in the units container that make up a whole.

So, if you base laying out content for a 12 column grid. A main-content column that should span 8 columns would include the mixin `grid-unit(8,12)` and the sidebar could include `grid-unit(4,12)`, this would make it span 4 out of 12 columns.

In this example Fraction grid will generate `width: 66,66666%` for the main-content column and `width: 33.33333%` for the sidebar.

Maybe these widths seem familiar? Well yes, 4 out of 12 is basically the same as the fraction 1/3 which is equal to 33.3333%.

This means that Fraction grid can be structured by thinking in terms of grid columns, or regular fractions, such as 1/3, 2/5 etc.

The responsiveness
------------------

Fraction grid's 'responsiveness' comes from the fact that every width is based on the relative '%', even the gutters. This makes the layout super fluid.

Also, the way column widths are applied with mixins works neatly with media queries. We can simply handpick what `grid-unit` mixins we need for a specific layout unit for different media queries.

The details
-----------

The demo covers pretty much the basics of Fraction grid. But at this moment, it doesn't do the best job at explaining everything that is going on and how all the thinking goes. 

I promise to sort that out soon.
















 