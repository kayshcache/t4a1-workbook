# T4A1 - Developer Workbook
{Fullname}__T4A1.zip

## Q1 Provide an overview and description of a standard source control process for a large project
The git repository must be created first and connected with a remote repository so that all the developers can commit to it. The collaborative workflow usually starts with the individual developers forking the repo and branching from their own branch.
Every morning a fetch/pull would likely be performed by the participating team members to conform the code across working environments.

Commits mark work completed to whatever fine degree:
- Infinitive verbs start git commit messages so that it reads like a set of instructions later.
- Commit messages should explain why a commit was made. If bugs are found the commits may be needed to locate them.

Pull requests merge branches to the master branch on the primary repo:
- Use branching to work on new features, branch from master when working on fixes or new features, the branch names should be very descriptive.
- Pull requests can initiate discussion between developers or teams to determine changes planned for merging.
- It's possible to deploy branches to test the code running in production
- Finally merging to master

## Q2 What are the most important aspects of quality software?
The most important aspects and characteristics of quality software are readability and code commenting. Reusable code, integrity, reliability, and confidentiality. Two important charactistics of note are readability and changeability - code that is descriptive/declarative. Readability can be improved by the use of sensible naming conventions for functions and variables as well as a sensible and conventional directory structure, the MVC pattern persists as an important archetype. It also refers to the awareness and mitigation of side-effects. Changeability would also refer to a modularized code base.

Additional points about quality code to be raised and explored in future quality written assignments may include but not limited to:
- usability design considers the user experience
- using too many acronyms is a career limiting moves
- secure up and down the stack
- semantic versioning
- separation of concerns: presentation logic (platform agnostic, ), business logic (eg. data fetching, user account behavior, application specific )
- always follow conventions - "depart from them at your peril." - Someone once said.
- single responsibility principle
- get it working, get it right, get it efficient
- common language referring to the Gang of Four
- test driven development lifecycle
- fit for purpose: does what's expected
- resource frugality
- latency/throughput efficiency

## Q3	Outline a standard high level structure for a MERN stack application and explain the components
MERN is comprised of a distinct front and backend, it's effectively 2 separate applications written with Javascript utilizing 4 key technologies:
Mongo is a NoSQL db that can be installed on the system with the backend or elsewhere.
Express is a server framework for use with NodeJs, it abstracts a lot of the code required to produce an HTTP web server. This can often be known the server or API
React is a frontend framework first and foremost for producing a web UI that communicates with a backend to read and write data from the database. This component is typically referred to as the React App or simply frontend.
NodeJS is a Javascript platform running on the Chrome V8 Engine and allows developers to run Javascript applications on a system outside of where JS used to be typically run, a browser.
These technologies are leveraged and combined to produce hosted web applications.
In terms of components, as there are typically 2 or more distinct applications in a MERN stack, both the API and React App contain source code for the running of their respective business logic. The separation of concern can differ greatly depending on the kind of application way the stack is comprised. React composes UI components and concerns itself primarily with user interaction and display of content. Whereas the API manages the important business functions and CRUD operations for the datastore.

## Q4	A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
Such a team ought to employ some of guidance offered by agile project management methodologies. Particular documentation is extremely useful for ensuring a project is seen to its end while also meeting the needs of its key stakeholders. Client liason is very important within this domain in terms of managing expectations and mitigating scope creep and other stakeholder risk management.
Web development and design might be needed for the creation of website, however, if it is simply a site and not web application or native mobile app, then said team ought to use Wix or another platform SaaS type solution. Overall an awareness of the appropraite solution to use for a "website" is essential - avoiding the re-invention of the wheel paramount. If this project requires serving dynamic database content with business logic then the following knowledge and skills would be required: at its highest level, full stack or serverless web development. Anyone creating a bespoke website would need to know all the aspects related to the above and throughout the development lifecycle be aware of OWASP top ten list of "Web Application Security Risks" https://owasp.org/www-project-top-ten/

## Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges
T3A3 Required that I make decisions about where to process the data. It was possible to work with the data using SQL or process it in the server side or on the front. Knowledge relating to the capabilities of each technology working together was vital to make such decisions. The patience of debugging and anticipating bugs was important in order to not feel defeated and carry on. There is always the urge to over engineer, to move towards a generic paradigm and cover increasing numbers of conceivable use cases. It has been an important skill, almost an instinct, to cultivate a resilience to digression from the programming problems at hand and focus on reaching viable solutions. Conversely, as I stepped into a solution for handling the connection methods to the SQL db, I recognized that I was still mostly incapable of knowing how to make use of OOP in a way that isn't merely a pointless academic exercise for demonstrating the principles of Object-based programming - throughout the endeavor it came up not to be defeated or overwhelmed by the volume of time wasted doing this bootcamp and try to focus on covering the ground one needs to get a rounded exposure to advanced programming techniques. With the tremendous volumes of information and opinion online today I time and time again must increase the sophication of selectively narrow scope.

## Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature
T3A3 My knowledge of specifics within technologies was limited, however, the skill of figuring out the solutions to any problems that I encounter was well established. By being persistent and calm, learning each thing in turn while keeping a low stakes serenity I was able to debug as well as make decisions about what path to use to proceed with the project. 

## Q7	Explain control flow, using an example from the JavaScript programming language
In the context of web development, control flow guides the logic of a program as it processes data or organizes layout and interactivity of components.
It can be achieved via a number of approaches. Some examples of methods of control flow available in JavaScript are:
- If conditional statements 
- Logic switching operators such as, || &&
- Loops combine with conditionals to create powerful ways to iterate through data and organize or reorganize it.
- More are....

## Q8	Explain type coercion, using examples from the JavaScript programming language
Type coercion can be achieved with JavaScript in a number of ways.
- explicit type casting - numbers and other primitives can be coerced to string with the function Boolean(x) Number(x) String(x)
- The loose equality operator (==) does some implicit type coercion.
- implicit coercion is done on a value or expression when placed in a conditional statement or used with logical operators, it is coerced to boolean.
- When using logical operators, the coercion is done internally, the original operands are returned by the expression
- The Object prototype has .valueOf() and .toString() methods available for derived types for explicit coercion.

https://www.freecodecamp.org/news/js-type-coercion-explained-27ba3d9a2839/

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
JSON is a standard structure and syntax for object nested data that can be handled in many programming languages. In a simple way, it is a text string shared between APIs that describes data in a structure that is similar to the Object.prototype of JavaScript. The string can be parsed into JS using the parse method of the JSON object in Javascript. Vice versa JSON can be created with the stringify method.
- JSON.parse() JSON.stringify()

## Q13	For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes
``` javascript
// Class declaration syntax - said to be sugar for declaring objects since its incorporation in ES6.
class Car {
// constructor function builds objects when they are declared
  constructor(brand) {
// the this keyword declares the properties of the object created with the class
    this.carname = brand;
  }
// object methods that all objects receive upon instantiation.
  present() {
// Methods can return just like functions
    return 'I have a ' + this.carname;
  }
}

// Inheritance from the class mentioned in the extends statement incorporating all of the properties and methods
class Model extends Car {
  constructor(brand, mod) {
// The super statement declares the properties of the parent class
    super(brand);
// New properties specific to the child class are also declared with the this keyword
    this.model = mod;
  }
  show() {
// The methods from the parent class are available to the child
    return this.present() + ', it was made in ' + this.model;
  }
}

// Declares an array of strings that can presumably be used as brand arguments for the create of objects
let makes = ["Ford", "Holden", "Toyota"]
// Array from method creates an array from another object. Here the 'new' operator is used to call the constructor in the Array prototype and argument passed indicating the length of the array to be created. As the second argument of the from() method, the anonymous arrow function is given to map over the new array incrementing by returning 1980 plus the index number. Producing an array of years counting 40 years from 1980.
let models = Array.from(new Array(40), (x,i) => i + 1980)

// Function takes two arguments and returns a random number in a given range
function randomIntFromInterval(min,max) { // min and max included
// Math.floor rounds a number down. .random returns a decimal number between 0 and 1.
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {
// For loop loops over the models array and produces a car/model object, rather arbitarily, as many cars as the length of the models array. Selects at random from one of the 3 makes then selects a model year also randomly and uses this fascinating information to create an exhilarating ride into more meaningless examples of using classes that apply to nothing but this idiotic example.
  make = makes[randomIntFromInterval(0,makes.length-1)]
// Such genius - i presume it's intentional to limit the model range to 1980-82 (0, 2)
  model = models[randomIntFromInterval(0,makes.length-1)]
    
// Instantiate a Model object that inherits its meaningless properties and methods from the Car class.
  mycar = new Model(make, model);
// log the return value from the model object to the console because that's what javascript is for.
  console.log(mycar.show())
// This is the closing curly bracket, it couldn't have come sooner.
}
```
## Marking Criteria
- CMP1043-2.1 Provide an overview and description of your source control process: Provides an extensive overview and description of a standard source control process
- CMP1043-2.2 What are the most important aspects of quality software? List discuss and demonstrate 6 software quality characteristics.
- CMP1043-2.3 Demonstrate sound design Architecture: Shows almost flawless understanding of the high level structure of the app
- CMP1043-3.1 A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project? Effectively describes a range of skills and knowledge required by IT workers to complete a quality web development project
- CMP1043-3.2 Within your own project what knowledge or skills were required to complete your project, and overcome challenges? Effectively describes a range of skills and knowledge used to complete a project.
- CMP1043-3.3 Evaluate how effective your knowledge and skills were this project, and suggest changes or improvements for future projects of a similar nature? Evaluates effectiveness of knowledge and skills accurately, providing examples, and providing an insightful improvement on each skill
- PRG1006-3.1 Explains the concept of control flow in programming: Provides a thorough explanation of control flow in programming
- PRG1006-3.2 Explains the concept of type coercion in programming: Provides a thorough explanation of type coercion in programming
- PRG1006-3.3 Explains the concept of data types in programming: Provides a thorough explanation of data types in programming
- PRG1006-5.1 Demonstrates an ability to manipulate arrays: Demonstrates an extensive ability to manipulate arrays
- PRG1006-5.2 Demonstrates an ability to manipulate objects: Demonstrates an extensive ability to manipulate objects
- PRG1006-5.3 Demonstrates an ability to manipulate JSON: Demonstrates an extensive ability to manipulate JSON
- PRG1006-4.1 Recognise functions, ranges and classes & PRG1006-4.2 Identify functions, ranges and classes: Demonstrates an extensive ability to recognise functions, ranges and classes
