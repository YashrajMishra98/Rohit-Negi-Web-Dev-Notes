<!-- Primitive Datatypes -->

let num = 10;  
let str = Alpha;
let bool = true;
let n = null; null is of object datatype typeof n = object
let und = undefined;
let big = 293867296589263592n; if we write n at the end it will be bigint

<!-- Non Primitive Datatypes -->

Array, Object, function

<!-- Array -->

let arr = [1, 4, "alpha", null] array is of object datatype typeof arr = object

<!-- Object -->

let obj = {
key1: "value1",
key2: 123,
"key 3": "beta"
}

<!-- to access the keys of object -->

console.log(obj.key1);
console.log(obj["key2"]);
console.log(obj["key 3"]);

<!-- Function -->

let fxn = function(){
code to be executed
}

function fxn(){
code to be executed
}

<!-- to check type of variable -->

typeof bool;

<!-- to print maximum and minimum integer -->

let max = Number.MAX_SAFE_INTEGER;
let min = Number.MIN_SAFE_INTEGER;

<!-- Type conversion -->

let str = "34";

<!-- two methods to convert into number -->

let num = Number(str);
let num = +str;

<!-- to convert into string -->

let str = String(num);

<!-- to convert into boolean -->

let bool = Boolean(str);

<!-- Operators -->

console.log(23%3); modulo operator prints the remainder 2
let sum = 2;
sum++ post increment operator
++sum pre increment operator
sum-- post decrement operator
--sum pre decrement operator
sum \*= sum;

to solve an mathematical operation first solve divide and multiply from left to right and then solve addition and subtraction from left to right

<!-- Comparison Operator -->

a == b checks if value of a and b are equal
a === b checks if both the value and type of a and b are equal
null == undefined true
null === undefined false
null == 0 false
null < 0 false
null > 0 false
null >= 0 true
null <= 0 true
NaN == NaN false

<!-- Bitwise Operator -->

& -> and
| -> or
^ -> xor
5<<3 5*2^3 = 40 left shift 5 by 3
20>>2 20*2^(-2) = 5 right shift 20 by 2

<!-- Lecture 5 -->

<!-- Primitive vs Non Primitive Data type -->

Primitive Data Type is Immutable(can't be changed)
Non Primitive Data Type is Mutable(can be changed)

let a = 10;
let b = a;
b = 30; only b will be changed a will remain 10 (immutable) b will be given new memory location
and then 30 will be assigned to it does not overwrite b but assign new memory location

but in case of Non Primitive Data Type
let obj1 = {
id: 20,
name:"alpha"
}

let obj2 = obj1;
obj2.id = 40; it will change the id of obj1 also i.e., obj1.id = 40 and obj2.id = 40 (mutable)

Primitive data types are stored in stack
Non Primitive data types are stored in Heap

<!-- Lecture 6 -->

if we want to use javascript variable then we can use backticks and dollar sign to use it dynamically
let price = 284;
console.log(Price is ${price});

<!-- String concatenation -->

let s1 = "Hello";
let s2 = "World";
let s3 = s1 + s2; s3 = HelloWorld

<!-- to get length of string -->

let length = s1.length;

<!-- to access the characters at particular index -->

console.log(s1[4]); prints o
console.log(s2.charAt(4)); prints d

s1.toLowerCase();
s1.toUpperCase();
s3.indexOf("Wor"); prints 5
s3.lastIndexOf("Wor"); prints the index of last occurence of Wor which is 5 in s3
s3.includes("lloW"); prints true as lloW is present in s3

s3.slice(start_index, last_index); includes start_index but excludes last_index
s3.substing(start_index, last_index); it also includes start_index but excludes last_index

slice can take negative index also but substring can not

s3.replace("old_string", "new_string"); old_string will be replaced by new_string
s3.replaceAll("old_string", "new_string"); old_string will be replaced by new_string

<!-- str.split(delimiter) : Splits a string into an array based on a delimiter -->

let str = "Alpha, Beta, Gamma, Delta, Bravo";  
console.log(str.split(", ")); prints ['Alpha', 'Beta', 'Gamma', 'Delta', 'Bravo']

str.trim() Removes whitespace from both ends
str.trimStart() Removes whitespace from start
str.trimEnd() Removes whitespace from end

Any Datatype created using new keyword it will be of object type
let arr = new Array(9).fill("E"); typeof arr is object, creates an array of size 9 and initializes with E
let string = new String("Hello world"); typeof str is object
let num = new Number(45); typeof num is object

<!-- Lecture 7 -->

let num = 231.68;
num.toFixed(3); fix to 3 decimal places = 231.680
num.toPrecision(4) round off to 4 digits = 231.7
num.toPrecision(2) round off to 2 digits = 2.3e+2
num.toExponential(3) converts into 3 digits and exponent = 2.32e+2
num.toString(); converts into string

<!-- Math -->

let e = Math.E; e = 2.7182818459045
let ln = Math.LN10; ln = 2.30258509299
let pi = Math.PI; pi = 3.141592653
let random = Math.random(); generates number 0 <= random < 1
Math.floor(e); floor value of e = 2
Math.ceil(pi); ceil value of pi = 4

<!-- To generate random value from min to max -->

let random = Math.floor(Math.random()\*(max - min + 1) + min);

<!-- Lecture 8 Array -->

<!-- methods to declare and initialize an array -->

const arr = [1, 2, "alpha", null, undefined, true];
const arr = new Array();
let arr = new Array(4); if single number is given then it will be considered as size of array
let arr = new Array(1, 2, "alpha", null); array will be initialized with given elements
arr.length; to get length or number of elements in array

<!-- to access elements of array at different indexes -->

arr[index]; it does not take negative index
arr.at(index); it also takes negative index

<!-- deep and shallow copy -->

shallow copy : both points to same array, changes in one will reflect in other
deep copy : both points to different arry, changes in one will not reflect in other

const arr = [1, 2, 3, 4, 5];
const arr1 = arr; shallow copy
const arr1 = structuredClone(arr); deep copy
const arr1 = [...arr]; deep copy

<!-- operations on array -->

arr.push("Alpha"); push function adds elements at end
arr.pop(); pop function deletes the last element
arr.unshift(32); unshift function adds elements at start
arr.shift(); shift function deletes the first element
arr.delete(arr[2]); deletes the given element but it leaves the space and a hole will be created
arr.indexof(4); gives the index of first occurence of 4
arr.lastIndexof(4); gives the index of last occurence of 4
arr.includes(3); checks if 3 is present in the array or not
arr.slice(starting_index, ending_index); slice the portion of array includes starting_index but excludes ending_index
arr.splice(starting_index, number_of_elements); splice the portion from starting index and takes number_of_elements elements, it changes  
 original string original array will not includes spliced elements

arr.splice(starting_index, number_of_elements_to_delete, value_of_elements_to_add);
arr.splice(2, 2, "alpha", null); arr = [1, 2, 'alpha', null, 5]
arr.toString(); arr = 1, 2, alpha, null, 5
arr.join("-"); arr = 1-2-alpha-null-5, it also converts into string
let arr2 = arr.concat(arr1, arr3, arr4); concat and converts into single array
arr.push(arr1); arr becomes 2D array containing arr1

let arr2d = [[1, 2], [3, 4, [7, 8, 9, [12, 34]]], [5, 6]];

<!-- if we want to convert it into 1D array -->

let arr = arr2d.flat(4); goes to 4 level to convert into 1D array
let arr = arr2d.flat(Infinity); if we don't know the dimension of array
console.log(Array.isArray(arr)); checks if arr is array or not returns true or false

<!-- Lecture 9 Date in JS -->

const d = new Date(); d = YYYY-MM-DDT02:56:10.922Z, after T international time zone is given
const d1 = d.toDateString(); d1 = day month date year
const d2 = d.toString(); d2 = Sun Jul 27 2025 08:52:25 GMT+0530 (India Standard Time)
const d3 = d.toISOString(); d3 = 2025-07-27T03:23:54.545Z
const d = Date.now(); d = milliseconds from January 1 1970, 00:00:00

const d = new Date(milliseconds); d = date calculated from january 1 1970, 00:00:00
d.getDate(); gives date
d.getDay(); gives day 0 for sunday and 6 for saturday
d.getMonth(); gives month 0 for january and 11 for december
d.getFullYear(); gives year
d.getMilliseconds(); gives milliseconds of today not from january 1 1970
d.getMinutes(); gives minutes
d.getTime(); gives milliseconds from january 1 1970, 00:00:00

newDate("YYYY-MM-DDTHours:minutes:seconds"); in string format 1 is for january and 12 is for december
new Date(YYYY-MM-DDTHours:minutes:seconds); in number format 0 is for january and 11 is for december
new Date(year, month, day, hours, minutes, seconds, milliseconds)
new Date(2025, 6, 12, 9, 34, 23, 234);

<!-- Setting Date Components -->

const d = new Date();
d.setDate(20);
d.setMonth(3);
d.setFullYear(2025);

<!-- date calculation -->

const date1 = new Date();
const date2 = new Date("2025-4-27");
const remaining = date2 - date1; remaining will be in milliseconds

<!-- Lecture 10 Object in JS -->

const obj = {
key:value,
key:value,
key:value
}

const obj = {
0:23,
1:45,
2:56,
name:"alpha",
"account balance": 345,
gender:"male",
"age":40
}

<!-- Methods to access value of object -->

obj.name;
obj["account balance"];
obj["gender"]; to access using square bracket key should be in string format
obj['0'];
obj["1"];
obj[2]; in number we can access without string

<!-- to delete any key value pair in object -->

delete obj.key;

<!-- class method to create object -->

class People{
constructor(name,age,gender){
this.name = name;
this.age = age;
this.gender = gender;
}
}

let P1 = new People("alpha", 20, "male");

Object.keys(obj); gives the array of keys of obj
Object.values(obj); gives the array of values of obj
Object.entries(obj); gives 2D array of key value pair of obj

<!-- to combine multiple objects in one object or to merge objects -->

Object.assign({}, obj1, obj2, obj3); it will assign all key value pair to the first object inside the paranthesis
const obj = {...obj1, ...obj2, ...obj3}; spread operator : same as the assign operator
assign operator creates deep copy in non nested object

<!-- Lecture 11 Object in JS part 2 -->

const obj = {
name:"alpha",
age:34,
gender:"male"
}

let obj1 = obj; shallow copy will be created
let obj2 = structuredClone(obj); deep copy will be created

<!-- Nested object : object inside an object -->

const user = {
name:"alpha",
balance:234,
address:{
pincode:278173,
city:"beta"
}
}
user.address.pincode; to access pincode

const user1 = Object.assign({}, user); deep copy of non nested keys will be created and shallow copy of nested keys will be created
const user2 = structuredClone(user); deep copy of all keys will be created

<!-- Destructring of an object -->

let obj = {
name:"alpha",
money:435,
balance:445,
age:34,
gender:"male"
}

const {name:me, money, ...obj1} = obj; name will be changed to me, all other keys will be stored in obj1 object known as rest operator
we can do the same with array using square brackets

<!-- In nested object destructring -->

const {address:{pincode, city}} = user;

obj._proto_ = user; now obj can use the keys of user
obj.hasOwnProperty(key); checks if key is present or not

<!-- Lecture 12 Function in JS -->

function fxn_name(parameters seperated by commas without using let, var or const){
code to be executed
return statement
}

const fxn_name = function(parameters){
code to be executed
return statement
}

<!-- Arrow function -->

const fxn_name = (parameters)=>{
code to be executed
return statement
}

<!-- if there is only single parameter and only return statement is under curly brackets then  -->

const fxn_name = parameter => parameter*5; parameter*5 will be returned

<!-- if number of parameter is not sure then use rest operator -->

const fxn_name = function(...number){
console.log(number);
}

<!-- Lecture 13 Loops -->

switch case
switch(new Date().getDay()){
case 0:
console.log("Sunday");
break;
case 1:
console.log("Monday");
break;
case 2:
console.log("Tuesday");
break;
case 3:
console.log("Wednesday");
break;
case 4:
console.log("Thursday");
break;
case 5:
console.log("Friday");
break;
case 6:
console.log("Saturday");
break;
default:
console.log("Not a valid Day");
}

<!-- Lecture 14 Advance Loops -->

let obj = {
name:"alpha",
age:34,
gender:"male",
balance:324
}

<!-- for in loop -->

for(let key in obj){
console.log(key, obj[key]); iterate over keys
}

<!-- for of loop -->

for(let value of arr){
console.log(value); can't be used for object
}

<!-- for each loop -->

arr.forEach(callback_function);
arr.forEach((num_or_value, index, arr)=>{
console.log(num);
console.log(arr[index]);
})

for in loop sabhi keys ko iterate karta hai jo object ki khud ki hai aur jo usne inherit kiya hai obj.**proto** = obj1 or obj = Object.create(obj1) lekin Object.keys(obj) sirf unhi keys ko iterate karta hai jo obj ki khud ki hai inherit wale ko iterate nhi karega

Object.getOwnPropertyDescriptor(obj, 'name_of_key');
output of above statement is given below
{
key:value,
writable:true,
enumerable:true,
configurable:true
}

if writable is true then we can change the value of the key
if configurable is true then we can change the value of writable and enumerable to true or false and property can be deleted
if enumerable is true then if we print the object it will print that key value pair and if enumerable of any key is false then that key value pair will not be printed

<!-- To change the properties of keys -->

Object.defineProperty(obj, 'key',{
key:value,
writable: true or false,
enumerable: true or false,
configurable: true or false
})

<!-- if for name writable is false then we can't change name -->

obj.name = "beta"; it will not work

<!-- if writable and enumerable is true and configurable is false the we can't change writable -->

Object.defineProperty(obj, 'name',{
writable: false, writable will remain true as configurable is false and it will not allow to change
enumerable: false as configurable is false so it will not allow to change the value of enumerable
})

<!-- Lecture 15 Callback function, Filter and Map  -->

setInterval(callBack_function, time_Interval_in_milliseconds); callBack_function will be executed after every time_interval

<!-- filter -->

arr.filter(callBack_function);
let arr = arr.filter((value, index, arr)=>value>19); selects the value if it satisfies the condition, asks true or false
if return is true the value is selected if false then not selected

<!-- map : modifies the array -->

let arr1 = arr.map((value, index, arr) => num\*5); each element of arr will be multiplied by 5 does not modify original array

<!-- Lecture 16 Reduce, sets and maps -->
<!-- reduce -->

arr.reduce(callBack_function, initialization);

const result = arr.reduce((accumulator, current)=>{
acc = acc+curr;
return acc;
}, 5); initially accumulator = 5 and current = arr[0]

<!-- set -->

let set = new Set([1, 2, 3, 4]); it contains unique value
set.add(5);
set.add("alpha");
set.size;
;set.delete(4);
set.has("alpha"); checks if alpha is present or not

<!-- array to set -->

let set = new Set(arr);

<!-- set to array -->

let arr = [...set];

<!-- union of sets -->

let set = new Set([...set1, ...set2, ...set3]);

forEach loop can be applied on set

<!-- maps : stores data in key value pair having unique key and maintains the order of insertion -->

const map = new Map();
map.set(key, value);
map.delete(key);
map.has(key);
map.size;
map.clear(); clears all keys and values from map and map becomes empty

<!-- another method to create and initialize map -->

const map = new Map([
[key, value],
[key, value],
[key, value]
])

to iterate on map we can use for of loop
for(let value of map{
console.log(value); print key value pairs
})

globalThis points to an global object

<!-- Lecture 19 DOM  -->
<!-- Methods to access elements -->

<!-- Using Id -->

document.getElementById('Id');

<!-- using className -->

document.getElementByClassName('class'); if multiple elements has same class then it gives an array of elements

<!-- using query selector -->

document.querySelector('CSS Selector');
document.querySelector('tag_name or .class or #Id, etc'); returns the first element having the given query
document.querySelectorAll('tag_name or .class'); returns the nodeList of elements

<!-- How to iterate over node list -->

const nodeList = document.querySelectorAll('tag_name or .class');

1.  nodeList.forEach((val)=>{
    console.log(val);
    })

2.  for(let val of nodeList){
    console.log(val);
    }

3.  for(let i=0;i<nodeList.length;i++){
    console.log(nodeList[i]);
    }

as nodeList is not an array we can not apply map, filter, reduce operations for this we have to convert it into array

<!-- to convert nodeList into array -->

const nodeList = document.querySelectorAll('tag_name or .class');
const arr = Array.from(nodeList);

<!-- using tag name -->

document.getElementsByTagName('tag_name'); Returns nodeList of alll elements with the specified tag name

<!-- Accessing using relationship -->

<!-- Accessing parent  -->

const element = document.querySelector('li');
const parent = element.parentNode; Access the immediate parent of the element
const parent = element.parentElement;

<!-- Accessing child -->

const element = document.querySelector('ul');
returns all the child elements
const child = element.childNodes; returns the nodeList of text present between the elements along with the elements
const child = element.children; returns only nodeList of child Elements

<!-- First and Last Child -->

element.firstChild;
element.firstElelmentChild;
element.lastChild;
element.lastElementChild;

<!-- Sibling Nodes -->

element.nextSibling;
element.priviousSibling;
element.nextElementSibling;
element.previousElementSibling;

<!-- Lecture 20 -->
<!-- Creating element -->

document.createElement('tag_name');

<!-- To insert the element inside other element -->

const parent = document.getElementById('Id');
const child = document.createElement('h3');

parent.appendChild(child); allows only one insertion

parent.append(child, child2, "Hello world!"); we can insert multiple elements and statements simultaneously

<!-- to insert text node  -->

const element = document.createTextNode("Hello world");
parent.append(element);

<!-- create and set attribute -->

const element = document.createAttribute('id');
element.value = "first";

const elem = document.querySelector('div');
elem.setAttributeNode(element); id = first will be set to the div

<!-- Accessing Attribute -->

const element = document.getElementById('Id');
element.getAttribute("id"); returns id
element.getAttribute("class"); returns className
element.getAttribute("style"); returns style

<!-- we can also set attribute -->

element.setAttribute("Attribute_name", "attribute_value"); Attribute_name="attribute_value"

<!-- to remove the attribute -->

element.removeAttribute("Attribute_name");

<!-- to add element at starting in an unordered list -->

parent.prepend(element); inserts before all the list items in the list

<!-- if we want to insert before specific element -->

parent.insertBefore(element_to_be_inserted, element_before_which_it_should_be_inserted);

<!-- to replace an element -->

parent.replaceChild(element_to_be_replaced, element_by_which_it_should_be_replaced);

parent.innerElement = HTML; another method to replace

insertAdjacentElement() or insertAdjacentHTML()
beforebegin: Before the element itself.
afterbegin: Inside the element, before its first child.
beforeend: Inside the element, after its last child.
afterend: After the element itself.

parent.insertAdjacentElement("beforebegin", element);
parent.insertAdjacentElement("afterbegin", element);
parent.insertAdjacentElement("beforeend", element);
parent.insertAdjacentElement("afterbegin", element);

<!-- delete node or element -->

element.remove(); this will delete the element

<!-- Lecture 22 Event in JS -->

element.addEventListener('event_name', callback_function);
element.addEventListener('event_name', (event)={ event is not compulsory parameter, its an event object
code to be executed
});

<!-- The third propertyy in addEventListener function is capture value which is false by default -->

if capture value is false it will perform bubbling and of true it will perform capturing
element.addEventListener('event_name', callback_function, capture(false by default))

<!-- Mouse Event -->

1. click
2. dbclick
3. mouseover
4. mousemove

<!-- Keyboard Event -->

1. keydown when key is pressed
2. keyup when key is released

<!-- Event Object -->

1. event It is an event object, it gives all the information about the event
2. event.target Refers to the DOM element that triggered the event
3. event.type tells you what kind of event occurred — as a string
4. event.key Refers to the key pressed on the keyboard
5. event.clientX The horizontal (X) coordinate of the mouse pointer relative to the viewport
6. event.clientY The vertical (Y) coordinate of the mouse pointer relative to the viewport

<!-- to read the data of input tag -->

first take access of the input tag
const input = document.querySelector('input');
const val = input.value; returns the data in the form of string
const value = +val; converts into number

setInterval function will execute the callBack_function after every given time interval
setInterval(callBack_function, timeInterval_in_milliseconds);

setTimeout is used to delay any function for given time
setTimeout(callback_function, delay_time_in_milliseconds);

<!-- Lecture 24 Forms in JS -->

form.addEventListener('click', (event)=>{
console.log(event);
console.log(event.target); returns which input is clicked
console.log(event.target.value); returns value of input
})

<!-- in place of click we can use other events also -->

1. input : returns value dynamically as we type
2. change : returns value when we type in an input box and get onto another input box
3. focusin : returns value of input box on which we focus or click to write
4. focusout : reurns value of input box when we move out of the input box
5. submit : form will be submit and refreshed
6. reset : page will be refresehed and data will be preserved

form.addEventListener('submit', (event)=>{
event.preventDefault();

    const first = document.getElementById('first');
    console.log(first.value);

    const second = document.getElementById('second');
    console.log(second.value);

});

<!-- if we have multiple inputs and we don't want to access each of them again and again then use FormData -->

const data = new FormData(form); data in key value pair is present inside data
const data_keys = Array.from(data.keys());
const data_values = Array.from(data.values());

data.keys() or data.values() or data.entries() returns an iterator

<!-- to iterate over iterator we can use for of loop -->

for(let key of data.keys()){
console.log(key);
}
