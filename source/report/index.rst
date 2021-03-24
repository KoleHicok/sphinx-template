React.js Report
================

**Thesis:** React.js
An overview of React.js and how it facilitates the creation of a dynamic page.

* Introduction

Background
----------

React.js was created to make web development more intuitive. React.js was
developed by Facebook and Instagram software architects to ease web page
modification via JavaScript. Typical web page manipulation requires
knowledge of the **Document Object Model** (DOM) and method calls that
manipulate the DOM. These methods often run slow and confuse most programmers.

Many companies, such as Facebook, Instagram, and Netflix, all use React because
it is fast and easy to use. This is because it is easier for programmers to
understand.([#f3]_) With no need for direct DOM interaction,
programmers can use JavaScript methods to do the work for them. This results in
a one-way data transfer. With this, the programmer can focus on their design
instead of the DOM's processes. This means companies spend less time training
new hires and more time developing new services.

When programming in React, there are a few concepts that allow easy construction
and manipulation of the user interface. The main building blocks of
React are **elements** and **components**. Elements are pieces of code that represent
changes that need to be made to the DOM. These are often written in
**JavaScript XML** (JSX) to make the code more readable and HTML-esque. These
elements are then rendered through components that make up the page. Components
are like functions that tell a browser how and where to load the page elements.

JSX is important as it simplifies the code from a method call for each element to
easy to use and understandable tags.([#f1]_) By combining these concepts, the
creation of a dynamic and reactive web page becomes a matter of adding elements
written in JSX to a component. We then render to the DOM using React's built in
`render()` method. This streamlined process allows companies and developers to
implement React for better a user and programmer experience.

* Advantages of React

  * Abstractions in components ([#f3]_)
  * Easier modular code
  * More secure from XSS
  * Easy site updates

    * Render method calls

* What is the virtual DOM

  * Document Object Model created on render of a web page
  * JavaScript can modify the DOM, but slowly and confusingly
  * React uses a virtual DOM stored in RAM to make quick adjustments

    * Finds differences between the current and previous virtual DOMs
    * Applies those changes in the real DOM

  * This makes DOM changes quick and easy

    * Only changes what's needed
    * Don't need to know what exactly needs to be changed in DOM

* Creating Elements

  * What are Elements?

    * Similar to a class that contains the code to build HTML

  * Elements are the instructions for component creation
  * Creating Elements using React.createElement
  * Element Children

    * Can contain other HTML tags for more complex page creation

* JSX

  * What is JSX ([#f5]_)
  * How does JSX simplify element creation
  * Translate JSX into React.create using Babel ([#f4]_)
  * Using JavaScript inside of JSX ([#f4]_) (Code snippet with {} notation)

* Rendering Components with Elements

  * JSON object containing a type of HTML tag
  * Props sub object for the attributes of the tag
  * Components are similar to a class that contains elements
  * This component is what is rendered into the virtual DOM

    * Once rendered, React then applies the changes to the DOM
    * Creates a one way flow of creation ([#f2]_)

* Conclusion

.. [#f1] Fedosejev, A., & Bush, A. (2015). React.js Essentials.
    Packt Publishing.

.. [#f2] Hunt, P., O’Shannessy, P., Smith, D., & Coatta, T. (2016). React:
    Facebook’s Functional Turn on Writing JavaScript. Communications of the ACM,
    59(12), 56–62. https://doi.org/10.1145/2980991

.. [#f3] Hunt, P. (2013, June 05). Why did we build react?. Retrieved February
    11, 2021, from https://reactjs.org/blog/2013/06/05/why-react.html

.. [#f4] Dodds, K. C. (2018, September 18). The introduction to React you've
    been missing. Lecture presented at 2018 UtahJS Conference. Retrieved
    February 10, 2021, from https://www.youtube.com/watch?v=SAIdyBFHfVU

.. [#f5] Chavan, Y. (2021, February 01). JSX in REACT – explained with examples.
    Retrieved February 11, 2021, from
    https://www.freecodecamp.org/news/jsx-in-react-introduction/