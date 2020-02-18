# T4A1 - Developer Workbook
{Fullname}__T4A1.zip
## Q1 Provide an overview and description of a standard source control process for a large project
The git repository must be created first and connected with a remote repository so that all the developers can commit to it. The workflow description goes here:

When the project is larger will everyone be on their own branch?
Pull requests merge branches ( does it merge the branch back into master? )
- Infinitive verbs start git commit messages so that it reads like a set of instructions later.

## Q2 What are the most important aspects of quality software?
The most important aspects and characteristics of quality software are readability and code commenting. Reusable code, integrity, reliability, and confidentiality.
- readability
- usability design considers the user experience
- career limiting moves
- secure up and down the stack
- semantic versioning
- separation of concerns: presentation logic (platform agnostic, ), business logic (eg. data fetching, user account behavior, application specific )

## Q3	Outline a standard high level structure for a MERN stack application and explain the components
Mongo
Express
React
Node

## Q4	A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
Project Management and Client Liason
Scope creep, stakeholder risk management, graphic design
web development: db, frontend/backend, server

## Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges
T3A3 Required that I make decisions about where to process the data. It was possible to work with the data using SQL or process it in the server side or on the front.

## Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature
T3A3 My knowledge of specifics within technologies was limited, however, the skill of figuring out the solutions to any problems that I encounter was well established. By being persistent and knowing fundamentals I was able to debug as well as make decisions about what path to use to proceed with the project.

## Q7	Explain control flow, using an example from the JavaScript programming language
In the context of web development, control flow guides the logic of a program as it processes data or organizes layout and interactivity of components.
It can be achieved via a number of approaches. Some examples of methods of control flow available in JavaScript are:
- If conditional statements 
- Logic switching operators such as, || &&
- Loops combine with conditionals to create powerful ways to iterate through data and organize or reorganize it.
- More are....

## Q8	Explain type coercion, using examples from the JavaScript programming language
Type coercion can be achieved with JavaScript in a number of ways.
- explicitly numbers can be coerced to strings with the operator .toString()

## Q9	Explain data types, using examples from the JavaScript programming language
Although JS is a loosely typed language, awareness of datatypes are very important.

## Q10	Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language
Array manipulation can be done by mutating arrays with loops using push, pop, and several other methods alter the items from the index. The return object from each of these methods varies. The set of methods available with the Array prototype in JS is quite extensive. There is also a selection of methods based on the _functional_ programming paradigm. Array.prototype.map() is a good example of manipulating array objects without mutating the original object. The map() method takes an array object and calls a provided function (can be an anonymous function or one declared elsewhere) on every index of the array and produces a new array. If the map() method is called without assigning the return array to another variable it might be that method won't produce any result in the application.

## Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language
Check points with educator:
- loops
- Object.entries()
- dot notation for static properties
- brackets for dynamic props

## Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language
- Parsing to objects JSON.parse() JSON.stringify()

## Q13	For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes
``` javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]
    
  mycar = new Model(make, model);
  console.log(mycar.show())
}
```
