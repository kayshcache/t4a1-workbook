# T4A1 - Developer Workbook
{Fullname}_T4A1.zip
## Q1 Provide an overview and description of a standard source control process for a large project
The git repository must be created first and connected with a remote repository so that all the developers can commit to it. The workflow description goes here:

## Q2 What are the most important aspects of quality software?
The most important aspects and characteristics of quality software are readability and code commenting. Reusable code, integrity, reliability, and confidentiality.

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
T3A3 My knowledge was limited, however, the skill of figuring out the solutions to any problems that I encounter was well established.

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

## Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

## Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

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
