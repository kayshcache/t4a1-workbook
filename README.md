# T4A1 - Developer Workbook
{Fullname}__T4A1.zip

## Q1 Provide an overview and description of a standard source control process for a large project
The git repository must be created first and connected with a remote repository so that all the developers can commit to it. The collaborative workflow usually starts with the individual developers forking the repo and branching from their own branch.
Every morning a fetch/pull would likely be performed by the participating team members to conform the code across working environments.

"Commits" mark work completed to whatever fine degree:
- Infinitive verbs start git commit messages so that it reads like a set of instructions later.
- Commit messages should explain why a commit was made. If bugs are found the commits may be needed to locate them.

Pull requests merge branches to the master branch on the primary repo:
- Use branching to work on new features, branch from master when working on fixes or new features, the branch names should be very descriptive.
- Pull requests can initiate discussion between developers or teams to determine changes planned for merging.
- It's possible to deploy branches to test the code running in production
- Finally merging to master followed by the working codebase for these team.

## Q2 What are the most important aspects of quality software?
The most important aspects and characteristics of quality software are numerous.
Readability and code commenting, Reusable code, Relatively secure so as to offer integrity, reliability, and confidentiality. Two charactistics of particular note are readability and changeability - code that is descriptive and declarative without comments. Readability can be improved by the use of sensible naming conventions for functions and variables as well as a conventional directory structure, the MVC pattern persists as an important archetype where apt. It also refers to the awareness and mitigation of side-effects. Changeability would also refer to a modularized code base.

Additional points about quality code to be raised and explored in future discussions may include but are not limited to:
- usability design considers the user experience of the end user and the extent that the application produced meets the business needs.
- using too many acronyms is a career limiting moves
- secure up and down the stack
- semantic versioning
- separation of concerns: presentation logic (platform agnostic, ), business logic (eg. data fetching, user account behavior, application specific )
- always follow conventions - "depart from them at your peril." - Someone once said.
- single responsibility principle
- get it working, get it right, get it efficient
- common language referring to the Gang of Four such as factory
- test driven development throughout the work lifecycle
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
Such a team ought to employ some of the guidance offered by agile project management methodologies. Particular documentation is extremely useful for ensuring a project is seen to its end while also meeting the needs of its key stakeholders. Client liason is very important within this domain in terms of managing expectations and mitigating scope creep and other stakeholder risk management.
Web development and design might be needed for the creation of website, however, if it is simply a site and not web application or native mobile app, then said team ought to use Wix or another platform SaaS type solution. Overall an awareness of the appropraite solution to use for a "website" is essential - avoiding the re-invention of the wheel paramount. If this project requires serving dynamic database content with business logic then the following knowledge and skills would be required: at its highest level, full stack or serverless web development. Anyone creating a bespoke website would need to know all the aspects related to the above and throughout the development lifecycle be aware of OWASP top ten list of "Web Application Security Risks" https://owasp.org/www-project-top-ten/

## Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges
T3A3 Required that I make decisions about where to process the data. It was possible to work with the data using SQL or process it in the server side or on the front. Knowledge relating to the capabilities of each technology working together was vital to make such decisions. The patience of debugging and anticipating bugs was important in order to not feel defeated and carry on. There is always the urge to over engineer, to move towards a generic paradigm and cover increasing numbers of conceivable use cases. It has been an important skill, almost an instinct, to cultivate a resilience to digression from the programming problems at hand and focus on reaching viable solutions. Conversely, as I stepped into a solution for handling the connection methods to the SQL db, I recognized that I was still mostly incapable of knowing how to make use of OOP in a way that isn't merely a pointless academic exercise for demonstrating the principles of Object-based programming - throughout the endeavor it came up not to be defeated or overwhelmed by the volume of things to know about in coding - try to focus on covering the ground one needs to get a rounded exposure to advanced programming techniques. With the tremendous volumes of information and opinion online today I time and time again must increase the sophication of selectively narrow scope.

## Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature
T3A3 My knowledge of specifics within technologies was limited, however, the skill of figuring out the solutions to any problems that I encounter was well established. By being persistent and calm, learning each thing in turn while keeping a low stakes serenity I was able to debug as well as make decisions about what path to use to proceed with the project. Drumming down well crafted encapsulation of related logic - in other words taking some more time to fully utilize Object based programming keeps coming up and I havent had the kind of exposure to know how to use it well in a practical context. Diagramming was an essential skill that requires more practice and reworking the original flow charts of ERDs for the project proved essential.

## Q7	Explain control flow, using an example from the JavaScript programming language
In the context of web development, control flow guides the logic of a program as it processes data or organizes layout and interactivity of components.
It can be achieved via a number of approaches. Some examples of methods of control flow available in JavaScript are:
- "If" conditional statements and ternary operator syntax: condition ? true outcome : false outcome
- Logic switching operators such as, || && are a great way to resolve resolve small value assignments and defaults.
- Loops combine with conditionals to create powerful ways to iterate through data and organize or reorganize it.
``` javascript
// This code uses primarily conditional statements to decide whether a user has attempted to authenticate with the correct password.
User.findOne({ email: req.body.email }, (err, user) => {
// Important to handle the error immediately
  if (err) res.send(err);
// Check for that user
  if (!user) {
    res.status(401).json({message: 'No such user'});
// in the case that use is found perform the check by utilizing a built in comparePassword method on the user object
  } else if (user) {
    if (!user.comparePassword(req.body.password, user.hashPassword)) {
      res.status(401).json({message: "Auth fail"});
// And if we get all this way through the control flow sequence, authenticate the user
  } else {
    return res.json({
      token: jwt.sign({
        email: user.email,
        username: user.username,
        _id: user.id}, JWT_KEY
      )
    });
  }
});
```

## Q8	Explain type coercion, using examples from the JavaScript programming language
Type coercion occurs explicitly through the use of functions that perform type coercion operations such as type casting. Implicitly values can be coerced as a side-effect of other operations performed with another intention. Coercion can be achieved with JavaScript in a number of ways. Explicit type casting - numbers and other primitives can be coerced to other types with the function Boolean(x) Number(x) String(x). Implicit coercion is done on a value or expression when placed in a conditional statement or used with logical operators, it is coerced to boolean. When using logical operators, the coercion is done internally, the original operands are returned by the expression. The loose equality operator (==) does some implicit type coercion. Numeric strings are also implicitly coerced during arithmetic operations for example, 20 - "10" = 10, however, the converse occurs with addition in the case of 20 + "20" = "2020". Build-in methods are also available in programming languages. The Object prototype has .valueOf() and .toString() methods available for derived types for explicit coercion.
``` javascript
render() {
  return (
    <>
    <UserComponent />
// The number is coerced to a string if it is found to be number
    <p>{type of this.state.phone === 'number' ? Number(this.state.phone) : this.state.phone}</p>
// Coercion is used internally of an expression to find a boolean value
    <p>{!this.state.user ? "No user found" : "Here they are!"}</p>
    <Footer />
    </>
  )
}
```
## Q9	Explain data types, using examples from the JavaScript programming language
Data types can be divided into classes, two data type classes present in JavaScript are primitive and composite. The primitive data types in JS are Number, Boolean, and String. Composite data types are made of more than one primitive type to form what is referred to as data structures. JS Functions, Objects and Array are all examples of composite data structures. Although JS is a loosely typed language, awareness of data types is very important. JavaScript is also said to hold two additional special data types, the two values 'undefined' and 'null'. Although they have slightly different characteristics to each other, when coerced to Boolean these two special types both become false. A remarkable character of JS is the lack of division of Number types, all JS Numbers are represented as floating-point numbers.
Although loosely typed TypeError can occur in JS - take the case of expecting an array in the state but getting undefined from an asynchronous function. An attempt to use map() with the value 'undefined' will result in a fatal type error and cease the application. Avoid this kind of error is acheived recently in React using Hooks. As seen below, by declaring what kind of objects in the state are expected, the code avoids errors without doing checks when it knows what it will receive from the fetch method in the proceeding useEffect method call:
``` javascript
// The types of expectant objects from asynchronous fetching methods using React Hook are declared in a state-like object until that data is available, effectively declaring types on the props
const [noticeInfo, setNoticeInfo] = useState({ name: '', hearts: 0, replies: [], posting: [] });

// contains async activity and props attempting to access the state may have errors if a temporary state object is not offered.
useEffect(() => {
  const fetchedData = async () => {
    const result = await fetch(`/api/notices/${name}`);
    const body = await result.json();
    setNoticeInfo(body);
  }
  fetchData();
}, [name]);
```
## Q10	Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language
Array manipulation can be done by mutating arrays with loops using push, pop, and several other methods alter the items from the index. The return object from each of these methods varies. The set of methods available with the Array prototype in JS is quite extensive. There is also a selection of methods based on the _functional_ programming paradigm. Array.prototype.map() is a good example of manipulating array objects without mutating the original object. The map() method takes an array object and calls a provided function (can be an anonymous function or one declared elsewhere) on every index of the array and produces a new array. If the map() method is called without assigning the return array to another variable it might be that method won't produce any result in the application.
```javascript
// Here we see 2 methods at work on the array would prefer remain untouched. First slice makes a shallow copy of the array we immediately alter and assign to a new constant.
// the filter array function performs a check using a callback include in the new array only nice things.
const niceArray = immutableMixedArray.slice().filter(thing => thing === nice);
```
## Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language
Loops can refer dynamically to object keys using square bracket notation offering ways to traverse an object iteratively. Dot notation is also available for retreiving properties or calling methods. When adopting a functional programming approach it may be useful to avoid mutation of objects completely in which case the freeze or seal methods may be used to restrict other objects or functions from modifying the object's data.
There are also a number of methods from the Object.prototype; one important example is Object.entries() - this method returns an array that resembles a map of key value pair arrays. The spread operator can merge objects to compose objects. When utilizing mixins with class declaration, composition can be favored over inheritance, one can use Object.assign() to compose additional properties or methods to a class and alter object literals after their constructor runs.
``` javascript
for (object in objects) {
  const keys = Object.keys(object);
  for (key in keys) {
    console.table(object[key]);
  }
}
```
## Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language
JSON is a standard structure and syntax for object nested data that can be handled in many programming languages. In a simple way, it is a text string shared between APIs that describes data in a structure that is similar to the Object.prototype of JavaScript. The string can be parsed into JS using the parse method of the JSON object in Javascript. Vice versa JSON can be created with the stringify method.
- JSON.parse() JSON.stringify()
```javascript
require('dotenv').config()
// One time i used the env to hold settings info in JSON and simply parsed it.
const appSettings = JSON.parse(process.env.SETTINGS_JSON);
```

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
// For loop loops over the models array and produces a car/model object, rather arbitarily, as many cars as the length of the models array. Selects at random from one of the 3 makes then selects a model year also randomly
  make = makes[randomIntFromInterval(0,makes.length-1)]
// code not lifted from w3schools contains a bug. Or is it intentional to limit the model range to 1980-82 (0, 2)?
  model = models[randomIntFromInterval(0,makes.length-1)]
    
// Instantiate a Model object that inherits its properties and methods from the Car class.
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
- CMP1043-3.1 Effectively describes a range of skills and knowledge required by IT workers to complete a quality web development project
- CMP1043-3.2 Effectively describes a range of skills and knowledge used to complete a project.
- CMP1043-3.3 Evaluates effectiveness of knowledge and skills accurately, providing examples, and providing an insightful improvement on each skill
- PRG1006-3.1 Explains the concept of control flow in programming: Provides a thorough explanation of control flow in programming
- PRG1006-3.2 Explains the concept of type coercion in programming: Provides a thorough explanation of type coercion in programming
- PRG1006-3.3 Explains the concept of data types in programming: Provides a thorough explanation of data types in programming
- PRG1006-5.1 Demonstrates an ability to manipulate arrays: Demonstrates an extensive ability to manipulate arrays
- PRG1006-5.2 Demonstrates an ability to manipulate objects: Demonstrates an extensive ability to manipulate objects
- PRG1006-5.3 Demonstrates an ability to manipulate JSON: Demonstrates an extensive ability to manipulate JSON
- PRG1006-4.1 Recognise functions, ranges and classes & PRG1006-4.2 Identify functions, ranges and classes: Demonstrates an extensive ability to recognise functions, ranges and classes
