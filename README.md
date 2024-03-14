# fCC Javascript Music Player
 Learn some essential string and array methods like the find(), forEach(), map(), and join(). These methods are crucial for developing dynamic web applications. The project covers fundamental concepts such as handling audio playback, managing a playlist, implementing play, pause, next, previous, and shuffle functionalities.

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
