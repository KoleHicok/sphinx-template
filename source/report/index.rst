Using React.js For More Dynamic Web Pages
=========================================

Creating a user interface (UI) is a difficult task. React.js helps web apps
engage the user with minimal effort. The web page becomes dynamic through
animated feedback to user input, making site navigation more interesting. It can
also easily display content from the server. This powerful JavaScript framework
allows a web developer to manipulate a web page as the user navigates the website.
React.js enables the creation of a single-page web app, rather than a set of
pages the user navigates through. Here we discuss React.js and how it aids in the
development of a dynamic UI.

.. image:: ../images/reactLogo.png
  :width: 45%
  :alt: React.js's Logo

Background
----------

React.js was created to make web development more intuitive. React.js was
developed by Facebook and Instagram software architects to ease web page
modification via JavaScript. Typical UI manipulation requires
knowledge of the **Document Object Model** (DOM) and method calls that
manipulate the DOM. These methods often run slowly as they refresh the entire DOM
and are less than intuitive.

Many companies, such as Facebook, Instagram, and Netflix, all use React because
it is fast and efficient. This is because it is easier for programmers to
use.([#f3]_) With no need for direct DOM interaction, programmers can use
JavaScript methods to do the work for them. This results in a one-way data
transfer from the script to the DOM. With this, the programmer can focus on
their design instead of getting and modifying DOM attributes. This means
companies spend less time training new hires and more time developing new services.

When programming in React, there are a few concepts that allow easy construction
and manipulation of the user interface. The main building blocks of
React are **elements** and **components**. Elements are pieces of code that represent
changes that need to be made to the DOM. These are often written in
**JavaScript XML** (JSX) to make the code more readable and HTML-esque. These
elements are made up of components. Components are similar to a class that tells a
browser how and where to load the page's elements.

.. code-block:: JavaScript
    :linenos:
    :caption: A comparison of using native JavaScript vs. React.js and JSX

    // Without React.js and JSX
    document.addEventListener("DOMContentLoaded", function(event) {
        // Making a new DOM element
        var paragraph = document.createParagraphElement();
        // Modifying the new element
        paragraph.innerText = "Hello World!";
        // Adding the new element to the DOM
        document.querySelector(".container").appendChild(paragraph);
    }

    // With React.js and JSX
    // React.js pushes the entire element to the DOM in one line of code
    ReactDOM.render(<p>Hello World!</p>, document.getElementByID('root'));

JSX is important as it simplifies the code from a method call for each element to
easy to use and understandable tags.([#f1]_) By combining these concepts, the
creation of a dynamic and reactive web page becomes a matter of adding components
written in JSX to an element. We then render to the DOM using React's built in
``ReactDOM.render()`` method. This streamlined process allows companies and developers to
implement React for better a user and programmer experience.

Advantages of React.js
----------------------

So why should you use React.js? There are a few major benefits. First,
abstractions allow for a more modular design. You can create
reusable UI components as a class. These classes then create components
in your elements. You can build your own abstractions in React.js. With an
abstracted and modular design, repeated or similar components
are easier to use within your site. This allows more flexibility and control over
the UI. It also eases the creation of repetitive UI elements

Second, React.js is more secure against **Cross-Site Scripting** (XSS) attacks.
This is because React.js natively escapes string variables.([#f3]_) Escaping strings
keeps potentially malicious code from being executed. This helps prevent the user
from executing scripts on your site and causing harm. While it is still a good
idea to sanitize all data, this is an added safe guard against such attacks.

Third, React.js allows for easier live updates to your UI. When a change is made,
the programmer simply makes a ``ReactDOM.render()`` method call with your changed
component. React.js finds the differences and applies the needed changes to the
DOM. This simplifies UI updates and the code needed for those updates. These
changes remain efficient as React.js only applies the changes to the DOM. The
unedited part of the UI remain untouched. This reduces the processing needed for
any changes, especially smaller changes. Along with this, the user experience is
smoother as there is no screen flicker when the DOM is emptied and repopulated.

The Virtual DOM
---------------

The **Document Object Model** (DOM) is a digital representation of a web page.
This representation is created as a web page is rendered in a browser. This
representation is what the computer uses to display a web page. Since the DOM is
created on loading a page, live changes to the DOM require JavaScript methods.
Typically these calls require specific and confusing method calls. These
methods make modifications confusing and unintuitive.

This is where React.js's virtual DOM comes into play. Firstly, using the virtual
DOM is more efficient because of how it modifies the DOM. Typically, a change to
the DOM requires emptying and rebuilding of the entire DOM. This can cause a
flicker on the screen while the DOM is empty. When React.js renders a change, it
first creates a new virtual DOM. This is then compared to the previous virtual
DOM. React.js finds the differences between these two representations. The
changes between the two virtual DOMs are then applied to the real DOM,
preventing a refresh and the aforementioned screen flicker.

The searching and changing all happens behind the scenes. This is because the
process only needs a ``ReactDOM.render()`` call and parameters containing the
component to render. React.js takes it from there. This simplification makes life
easier for a JavaScript programmer. Instead of learning about DOM calls and
modifications, they can simply use JSX's HTML-like syntax.

Having a program find and make changes may seem less efficient than manual
edits, but React.js is still quite efficient. This is primarily thanks to the
virtual DOM system. Since only the needed changes are applied to the DOM, the
whole process is quite fast. Each of these factors is why React.js is an
efficient and easy to use language or creating a positive user experience. This
is largely in part thanks to the virtual DOM.

Creating Components
-------------------

So what are components? They are what allow for the modular and abstracted
UIs React.js can create. Components are similar to a class that **encapsulates**
an element you want to create. Encapsulation is the process of creating a generalized
version of an object that can be modified to satisfy different requirements. By
encapsulating the more generalized portions of your elements, you can easily create
many similar elements for different needs.

Encapsulation is an important part of programming in React.js. This encapsulation
is largely what makes UIs easier to create expand upon in the framework.
The components created are the blueprint for elements that will be used in the
future. A component can be written as a class that extends the ``React.Component``
class. ([#f6]_) This flexibility in notation allows for those with different
tastes and styles to still use React.js comfortably. The following examples would
represent a paragraph tag using the specified font and child html:

.. code-block:: JavaScript
    :linenos:
    :caption: Examples of different ways to build components

    // Component as a function
    const Paragraph = ({ children, font }) => ({
        type: 'paragraph',
        props: {
            className: 'body-paragraph paragraph-' + font,
            children: {
                type: 'p',
                props: {
                    children: children
                }
            }
        }
    });

    // Components as a class
    class Paragraph extends React.Component {
        render() {
            const {children, font} = this.props;
            return {
                type: 'paragraph',
                props: {
                    className: 'body-paragraph paragraph-' + font,
                    children: {
                        type: 'p',
                        props: {
                            children: children
                        }
                    }
                }
            };
        }
    }

These two components, written in different styles, produce the same paragraph
with a different font and html in the paragraph tag. This allows a programmer to
use React.js in a way that is comfortable for them. This encapsulation makes UI
creation simple and modular once it is in place.

JavaScript  XML (JSX)
---------------------

Component creation can be further simplified with the use of JavaScript XML.
**JavaScript XML** (JSX) is a mark-up language that simplifies React.js
objects.([#f5]_) It does this through its syntax that resembles HTML. The
programmer doesn't have to understand ``React.createElement`` or React.js's object
notation. Instead, the HTML you already know can be used in JavaScript files to
create objects. This lowers the knowledge barrier for using React.js and makes the
code easier to read.

Since JSX is not actual JavaScript, we will need a translator to interpret the
JSX. A popular option for this is Babel. Babel is a compiler that can transform
syntax between languages, such as JSX and React.js. Babel even has a preset for
React.js that automatically sets up for this translation. Using Babel is as easy
as importing it through a script tag. This can be come from a site such as
unpkg.com.([#f4]_) Once you do this, Babel will automatically translate your JSX
into a ``React.createElement`` method call with the proper parameters.

So why do we need to do all of the extra configuration to use JSX? JSX allows
you to run JavaScript code inside of your tags. This is done using curly
bracket (``{}``) notation.([#f4]_) This is because Babel will not modify any text
within curly brackets. This allows access to variables and computations as you
create components and elements. Using template literal notation (``${}``) gives
you this same functionality from within a string. This makes code even more
readable and understandable for those programming and reading the code.

The previous example of a paragraph can be simplified to this:

.. code-block:: jsx
    :linenos:
    :caption: JSX simplification of a component

    class Paragraph extends React.Component {
        render() {
            const {children, font} = this.props;
            let element = (
                <p className = `body-paragraph paragraph-${font}`>
                    {children}
                </p>
            );
            return element;
        }
    }

As you can see, this notation is easier to read and understand than the object
notation in the previous example.

Rendering Elements
------------------

Once you are ready to render your UI to the DOM for the user to see, its time to
create elements and render them. Elements can be created in either of the
aforementioned ways, either by using the ``React.createElement()`` method or by
using JSX as a parameter for a ``ReactDOM.render()`` method call. These methods
convert the given parameters into a JSON representation of the element that the
``ReactDOM.render()`` method can use. This JSON representation contains the type
of HTML tag and a sub-object called props.

The props object contains information about the tag (id, className, etc.) and
the children of that tag. Elements can be made more complex HTML structures using
the props object. These nested tags are fairly simple to make, especially when
using JSX to make your elements. While the nested structure is easy to make, the
DOM changes remain more complex and dynamic to improve the user experience.

The resulting JSON object is what React.js uses to render the UI. It first locates
where in the UI the element will go. Then, a new virtual DOM is rendered to compare
with the previous version. This comparison results in the specific changes needed
to update the real DOM. These changes are then applied to the DOM and the UI is
updated. This one way flow of information is easier to understand and requires
less knowledge about DOM interaction and attributes.([#f2]_) React.js takes care
of those operations for the programmer.

Conclusion
----------

React.js is a simple and effective way to make dynamic and interesting user
interfaces. Through the use of components, elements, and JSX, a web developer
can achieve engaging results without the added confusion of DOM interactions.
After gaining a basic understanding of the language, dynamic interfaces can be
updated with easy to read and understand code. These are all reasons why
React.js is a powerful tool for the creation and updating of user interfaces.

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

.. [#f6] Abramov, D. (2015, December 18). React components, elements, and
    Instances – React blog. Retrieved April 05, 2021, from
    https://reactjs.org/blog/2015/12/18/react-components-elements-and-instances.html