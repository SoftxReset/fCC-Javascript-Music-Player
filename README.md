# fCC Javascript Music Player
 Learn some essential string and array methods like the find(), forEach(), map(), and join(). These methods are crucial for developing dynamic web applications. The project covers fundamental concepts such as handling audio playback, managing a playlist, implementing play, pause, next, previous, and shuffle functionalities.

Notes taken from this project:

- learn about the Web Audio API and how to use it to play songs. All modern browsers support the Web Audio API, which lets you generate and process audio in web applications.

- Your music player should keep track of the songs, the current song playing, and the time of the current song. To do this, you will need to create an object to store this information.

- The spread operator (...) allows you to copy all elements from one array into another. It can also be used to concatenate multiple arrays into one. In the example below, both arr1 and arr2 have been spread into combinedArr:

const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const combinedArr = [...arr1, ...arr2];
console.log(combinedArr); // Output: [1, 2, 3, 4, 5, 6]

- Now you need a way to display the songs in the UI (User Interface). To do this, you'll create a renderSongs function using the arrow function syntax.
- An arrow function is a shorter and more concise way to write functions in JavaScript. It's a function expression, which is a function that's assigned to a variable.

- The map() method is used to iterate through an array and return a new array. It's helpful when you want to create a new array based on the values of an existing array.

const numbers = [1, 2, 3];
const doubledNumbers = numbers.map((number) => number * 2); // doubledNumbers will be [2, 4, 6]

- Notice that the map() method takes a function as an argument. This is called a callback function, which is a function that is passed to another function as an argument. In the example above, the callback function is (number) => number * 2, and it's run on each element in the numbers array. The map() method then returns a new array with the results.

- The join() method is used to concatenate all the elements of an array into a single string. It takes an optional parameter called a separator which is used to separate each element of the array.

const exampleArr = ["This", "is", "a", "sentence"];
const sentence = exampleArr.join(" "); // Separator takes a space character
console.log(sentence); // Output: "This is a sentence"

- To chain multiple methods together, you can call the join() method on the result of the map() method.

array.map().join();

- Optional chaining (?.) helps prevent errors when accessing nested properties that might be null or undefined:

const user = {
  name: "Quincy",
  address: {
    city: "San Francisco",
    state: "CA",
    country: "USA",
  },
};

// Accessing nested properties without optional chaining
const state = user.address.state; // CA

// Accessing a non-existent nested property with optional chaining
const zipCode = user.address?.zipCode; // Returns undefined instead of throwing an error

- To sort the songs in alphabetical order by title, you will need to pass in a compare callback function into your sort() method.
- The sort() method accepts a compare callback function that defines the sort order.
- Strings are compared lexicographically which means they are compared character by character.
- Another use case for the callback function is to randomize an array.
- One way to randomize an array of items would be to subtract 0.5 from Math.random() which produces random values that are either positive or negative.
- This makes the comparison result a mix of positive and negative values, leading to a random ordering of elements.

- The find() method retrieves the first element within an array that fulfills the conditions specified in the provided callback function. If no element satisfies the condition, the method returns undefined

const numbers = [10, 20, 30, 40, 50];

// Find the first number greater than 25
const foundNumber = numbers.find((number) => number > 25);
console.log(foundNumber); // Output: 30

- Before playing the song, you need to make sure it starts from the beginning. This can be achieved by the use of the currentTime property of the audio object.

- (property and method for class and element, confusion) Next, use the classList property and the add() method to add the "playing" class to the playButton element. This will look for the class "playing" in the CSS file and add it to the playButton element.
- To finally play the song, use the play() method on the audio variable. play() is a method from the web audio API for playing an mp3 file.

- The indexOf() array method returns the first index at which a given element can be found in the array, or -1 if the element is not present.

- The forEach method is used to loop through an array and perform a function on each element of the array. For example, suppose you have an array of numbers and you want to log each number to the console.

- textContent sets the text of a node and allows you to set or retrieve the text content of an HTML element.

<div id="example">This is some text content</div>

const element = document.getElementById('example');
console.log(element.textContent); // Output: This is some text content

- createElement() is a DOM method you can use to dynamically create an element using JavaScript. To use createElement(), you call it, then pass in the tag name as a string:
// syntax
document.createElement(tagName)

// example
document.createElement('div')

const divElement = document.createElement('div')

- After created the button, you need to assign it a text. 
- To do this, you need to use the createTextNode() method of DOM.
- The createTextNode() method is used to create a text node.
document.createTextNode("your text")
- Assigning it to a variable
const myText = document.createTextNode("your text")
