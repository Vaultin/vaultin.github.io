---
layout: page
title: jQuery
permalink: /jQuery/
---

# jQuery reference

## Selector
### $ Selector

To select an element in jQuery you use this syntax:

    var $selcted = $('.className')

    var $selected2 = $('#idName')


its a convention to use a $ in front of variables that select a DOM object.

## jQuery functions


    $('.example-class').hide(); // Hides a element

    $('.example-class').show(); // Shows a element

    $('.example-class').fadeIn(400); // Fades in a element over 400 milliseconds

    $('.example-class').toggle(); // Toggles a element (shows and hides)

    $('.example-class').toggleClass('active'); // Toggles the class for all elements with class .example-class

    $(this).toggleClass('active'); // Toggles it only for THIS element we clicked on etc.

    $('.item-one').next().hide(); // selects the next element

    $('.my-selector').text('Hello world!'); // Adds text to a element or replaces text that is already there

    $('.example-class').slideToggle(400); // slides elements in over 400 milliseconds in this example

## Events
### on('click')

    $('.example-class').on('click', function() {
      // execute the code here when .example-class is clicked.
    });
