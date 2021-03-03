React.js Outline
================

**Thesis:** How to use React.js
React.js enables the creation of a reactive and dynamic web page.

* Background

  * Who created and uses React

    * Facebook invented React
    * Many companies with reactive sites use React.js

  * Why React is easier for programmers to understand ([#f2]_)

    * Less DOM interaction, focus on app and data
    * Ease of access for programmers

  * What are the basic concepts when programing React

    * Elements
    * Components

  * The importance of JSX ([#f1]_)

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