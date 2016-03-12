# AngularJS - "Not as Bad As You Think" ®

Angular has earned a pretty bad reputation among a lot of developers as being big, confusing, and hard to test.

To some extent, this reputation is deserved. But for the most part, the worst thing Angular did was offer **too much tooling with too little guidance**. With sane architecture and lots of discipline, it's easy to make an Angular app that's easy to test and easy to extend.

Which is not to absolve the framework of responsibility for its sins. Angular sometimes feels like a car with thousands of buttons and pedals and three or four steering wheels: it's possible to drive the thing safely on the highway, but you have to know a **lot** about how to drive it before you can use it without killing yourself. 

That's bad
==========

Angular is a fine framework for making fine applications, but you shouldn't need to be an expert in the tool to be able to use it safely.

Worse - the framework advertises some of its worst features as a way of getting new users through the door.


Example #1
==========
# CODE: index.html


The following ToDo application is made with literally 0 lines of JavaScript.
It is a piece of shit.

This is a *slightly* exaggerated version of the same garbage Angular advertises on its website.

Obvious problems:

1. testing would be horrible - it would have to be one big feature test
2. the view modifies the model directly
3. the markup contains logic-4-dayz®

Less obvious:

1. communicating between components would be hard
2. reusing code would be impossible
3. The app has no namespace. Check out the `ng-app` directive on the body tag. It is straight-up crazy that this is a feature that Angular permits, and it is 100% a free first hit of crack to make the framework feel inviting before you find yourself unable to understand where your code lives and you're living under a bridge


Is this really Angular's fault?
===============================

# CODE: todo_react.html

Let's look at the same garbage app in React:

Has Anyone Really Been Far Even as Decided to Use Even Go Want to do Look More Like?

Admittedly, this is contrived, but it's still unbelievable bad code, and it still works **perfectly** with React. 

Obvious problems:

1. testing would be horrible - it would have to be one big feature test
2. the the view is 100% illegible. you **cannot** read it at a glance
3. the markup contains one metric ass-ton of code

Less obvious:

1. we had to use a ref, which means we had to break out of the Component/DOM abstraction at the core of React
2. The file contains non-javascript masquerading as real JS. JSX is an amazing abstraction. It's good enough that I would not be surprised if it gets included in a future ES specification, but for now we're shipping an additional runtime with our code (`babel`); we could transpile our code beforehand, but the angular example does not do that. One way or another, this react example forces us to ship something other than what we actually use in the browser.









