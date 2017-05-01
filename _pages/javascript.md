---
layout: page
title: Javascript Reference
permalink: /javascript/
---


#Javascript reference
##Basics:
###Data types:

String -   grouping of words and/or numbers in single or double quotes.

Number -   any number including numbers with decimals.

Boolean -  truth value, true or false.

-----------------------------------------
###Variables:
always begin with the 'var' keyword.

    var something = 'a variable'

you can also reassign variables.

    something = 'now its something else'

###Escaping characters.
characters in Javascript are escaped with a \

    console.log('You\'re classy')

###Console functions:
console.log()

    console.log('This is a test')
    console.log('String 1', 'String 2', '.....')
    console.log('String with ', something)
    console.log('This' + ' is ' + 'a test')

###Operators:
standard math operators, + - / * and % (modulus, remainder).

    console.log((31 * 4) + 10 - (42 / 3))

###Modulus:
returns the remainder from a division.

    console.log(31 % 2)
this returns 1, 2 goes into 31, 15 times with a remainder of 1.

###Interpolation:
put variables into strings.

    console.log('This is' + something + '!')

##Control Flow:
###If/Else:
When the if is true, run that code, otherwise run the else code.

    var needCoffee = true;
      if (needCoffee) {
          console.log('Finding coffee');
          } else {
            console.log('Keep on keeping on!');
          }

Code between curly braces are called blocks. if/else statements have two code blocks.

    var stopLight = 'green';

    if (stopLight === 'red') {
      console.log('Stop');
      } else if (stopLight === 'yellow') {
        console.log('Slow down');
      } else if (stopLight === 'green') {
        console.log('Go!');
      } else {
        console.log('Caution, unknown!');
      }

###Comparison operators:
here they are:

+ Less than: **<**
+ Greater than: **>**
+ Less than or equal to: **<=**
+ Greater than or equal to: **>=**
+ Equal to each other: **===**
+ Not equal to each other: **!==**

###Logical operators:

+ Both must be true: **&&**
+ Either can be true: **||**
+ Make it opposite: **!**


    var truth = true

    if (!truth) {
      console.log('This will not run.')
    } else {
      console.log('But this will run!')
    }

    /*  Truth table

       true && true = true
       true && false = false
       false && true = false
       false && false = false

       true || true = true
       true || false = true
       false || true = true
       false || false = false */


###Switch statement:
for many else if statements, use switch instead.

        var groceryItem = 'papaya';

           switch (groceryItem) {
             case 'tomato':
               console.log('Tomatoes are $0.49');
               break;
             case 'lime':
               console.log('Limes are $1.49');
               break;
             case 'papaya':
               console.log('Papayas are $1.29');
               break;
             default:
               console.log('Invalid item');
               break;
             }

##Functions

###Declaring functions:

    function myName() {
      console.log('Test')
    }

###Calling functions:

    function myName() {
      console.log('Output')
    }

    myName()

###Variable scope:

    var globalScope = 'This is global'

    function myName() {
      var functionalScope = 'This is only available to this function'
      console.log(globalScope) // works
    }

    console.log(functionalScope) // doesn't work


## Loops
###For loop:

    var vacationSpots = ['New York', 'Tokyo', 'Paris']

    for (var counter = 0; counter < vacationSpots.length; counter++) {

      console.log(vacationSpots[counter])
    }

This loop could also go trough an array backwards, just set the counter variable to the length of the array minus 1 and the condition to the counter greater than or equal to 0, and the counter--.

    var vacationSpots = ['New York', 'Tokyo', 'Paris']

    for (var counter = vacationSpots.length; counter >= 0; counter--) {

        console.log(vacationSpots[counter])
    }

###While loop:

Loop while the argument is true.

    var argument = true
    while(argument) {
      console.log(argument)
      argument = false
    }

This loop only runs once, because I set the variable to false inside the loop.
