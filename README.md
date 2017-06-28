# BOOLEAN LOGIC EXERCISES

### Part 1
Write down what the following statements will return. Try to figure this out before putting the commands in the chrome console.


Answers:

1.) 2 == "2";
>true

2.) 2 === 2;
>true

3.) 10 % 3;
>true

4.) 10 % 3 === 1;
>true

5.) true && false;
>false

6.) false || true;
>true

7.) true || false;
>true


### Part II
Answer the following questions about this code block:

    var isLearning = true;
    if(isLearning){
        console.log("Keep it up!");
    } else {
        console.log("Pretty sure you are learning....");
    }

1. What should the above code console.log? Why?
 
 > The code should print "Keep it up!"

2. Why do we not need to specify if(isLearning === true)? Why does if(isLearning) work on its own?

>We do not need to specify it because condition in if-else statements will be forced into a boolean. It works on its own because isLearning value is true;


    var firstVariable;
    var secondVariable = "";
    var thirdVariable = 1;
    var secretMessage = "Shh!";

    if(firstVariable){
        console.log("first");
    } else if(firstVariable || secondVariable){
        console.log("second");
    } else if(firstVariable || thirdVariable){
        console.log("third");
    } else {
        console.log("fourth");
    }


1. What should the above code console.log? Why?
>It should console log "third" because it is the first conditional statement to satisfy its condition.
		
2. What is the value of firstVariable when it is initialized?
>undefined
		
3. Is the value of firstVariable a "truthy" value? Why?
>It's not a truthy value because it has a value of undefined and undefined is a falsy value.
		
4. Is the value of secondVariable a "truthy" value? Why?
>The secondVariable is not a truthy value because single quotes and double quotes are considered as falsy value.
		
5. The value of the thirdVariable is a truthy value because 1 is considered as true.
>Is the value of thirdVariable a "truthy" value? Why?

### Part III

Research Math.random here and write an if statement that console.log's "Over 0.5" if Math.random returns a number greater than 0.5. Otherwise console.log "Under 0.5".

	if (Math.random() < 0.5){
		console.log "Over 0.5";
	} else{
		console.log "Under 0.5";
	}


List of falsy Values:

	false 
	0 and -0
	NaN
	null
	undefined
	""
	''






# ARRAY EXERCISES
1. Using a loop, iterate through this array and console.log all of the people.
 ```
 for(i=0; i < people.length; i++){
	console.log(people[i]);
	
 }
```
2. Write the command to remove "Greg" from the array.
>people.shift();  // arr = ["Mary, "Devon", "James"]

3. Write the command to remove "James" from the array.
>people.pop(); // arr = ["Mary", "Devon"]
4. Write the command to add "Matt" to the front of the array.
>people.unshift("Matt"); // arr = ["Matt", "Mary", "Devon"]
5. Write the command to add your name to the end of the array.
>people.push("Jon"); // arr = ["Matt", "Mary", "Devon", "Jon"]
6. Using a loop, iterate through this array and after console.log-ing "Mary", exit from the loop. // ["Matt", "Mary"]
```
for(i=0; i < people.length; i++){
	console.log(people[i]);
	if (people[i] == "Mary"){
		break;
	}

	
 }
```
7. Write the command to make a copy of the array using slice. The copy should NOT include "Mary" or "Matt".
>arr2 = people.slice(2); // arr2 = ["Devon", "Jon"]

8. Write the command that gives the indexOf where "Mary" is located.
>people.indexOf("Mary");

9. Write the command that gives the indexOf where "Foo" is located (this should return -1).
>people.indexOf("Foo");
10. Redefine the people variable with the value you started with. Using the splice command, remove "Devon" from the array and add "Elizabeth" and "Artie". Your array should look like this when you are done ["Greg", "Mary", "Elizabeth", "Artie", "James"].
```
var people = ["Greg", "Mary", "Devon", "James"];
	
people.splice(2,1, "Elizabeth, "Artie");
```
11. Create a new variable called withBob and set it equal to the people array concatenated with the string of "Bob".
>var withBob = people.concat("Bob");
# OBJECT EXCERCISES
```
var programming = {
	languages: ["JavaScript", "Python", "Ruby"],
	isChallenging: true,
	isRewarding: true,
	difficulty: 8,
	jokes: "http://stackoverflow.com/questions/234075/what-is-your-best-programmer-joke"
};
```
1. Write the command to add the language "Go" to the end of the languages array.

>programming.languages.push("Go")

2. Change the difficulty to the value of 7.

>programming.difficulty = 7

3. Using the delete keyword, write the command to remove jokes key from the programming object.

>delete programming.jokes

4. Write the command to add a new key called isFun and a value of true to the programming object.

>programming.isFun = true

5. Using a loop, iterate through the languages array and console.log all of the languages.

```
for (var i= 0; i < programming.languages.length, i++)
{
	console.log(programming.languages[i]);
}
```


6. Using a loop, console.log all of the keys in the programming object.
```
for (var singleKey in programming){
	console.log(singleKey);
}
```
7.Using a loop, console.log all of the values in the programming object.
```
var programming = {
    languages: ["JavaScript", "Python", "Ruby"],
    isChallenging: true,
    isRewarding: true,
    difficulty: 8,
    jokes: "http://stackoverflow.com/questions/234075/what-is-your-best-programmer-joke"
};

for (var singleKey in programming){
	console.log(programming[singleKey]);
}
```

# FUNCTIONS
### difference

this function takes in two parameters and returns the difference of the two;
```
function difference(num1, num2){
	return num1 - num2;

}
```
### product
this function takes in two parameters and returns the product of the two;
```
function product(num1, num2){
	return num1 * num2;
}
```
### printDay
this function takes in one parameter (a number from 1-7) and returns the day of the week (1 is Sunday, 2 is Monday, 3 is Tuesday etc.). If the number is less than 1 or greater than 7, the function should return undefined;
```
function printDay(day){
	switch(day){
	case 1:
		return "Sunday";
	
	case 2:
		return "Monday";
		
	case 3:
		return "Tuesday";

	case 4:
		return "Wednesday";

	case 5:
		return "Thursday";
	case 6:
		return "Friday";
	case 7:
		return "Saturday";
	default:
		return undefined;
	}
}
```
### lastElement
this function takes in one parameter (an array) and returns the last value in the array. It should return undefined if the array is empty.

```
function lastElement(arr){
	return arr[arr.length-1];

}

```
### numberCompare
this function takes in two parameters (both numbers). If the first is greater than the second, this function returns "First is greater". If the second number is greater than the first, the function returns "Second is greater". Otherwise the function returns "Numbers are equal"
```
function numberCompare(num1, num2){
	if (num1 > num2){
	return "First is greater";
	
	} else if (num1 < num2){
	return "Second is greater";
	
	} else {
		return "Numbers are equal";
	}
}
```

### singleLetterCount
this function takes in two parameters (two strings). The first parameter should be a word and the second should be a letter. The function returns the number of times that letter appears in the word. The function should be case insensitive (does not matter if the input is lowercase or uppercase). If the letter is not found in the word, the function should return 0.
```
function singleLetterCount(word, letter){
	var letterCount = 0;

	for(var i=0; i<word.length; i++){	

		if (word[i].toLowerCase() === letter.toLowerCase()){
			letterCount = letterCount + 1;
		}	
	}

	return letterCount;
}
```

### multipleLetterCount
```
function multipleLetterCount(string){
	countMultipleLetter = {}
	for(var i=0; i<string.length; i++){


		var letterCount = 0;
		for(var j=0; j<string.length; j++){

			if (string[i] == string[j]){
				letterCount = letterCount + 1;
			}
		
		}
		
		countMultipleLetter[string[i]] = letterCount;

	}
	return countMultipleLetter;
}
```

### arrayManipulation

this function should take in at most four parameters (an array, command, location, and value).


If the command is "remove" and the location is "end", the function should remove the last value in the array and return the value removed. (In this case, the function only needs three arguments.)

If the command is "remove" and the location is "beginning", the function should remove the first value in the array and return the value removed. (In this case, the function only needs three arguments.)

If the command is "add" and the location is "beginning", the function should add the value (fourth parameter) to the beginning of the array and return the array.

If the command is "add" and the location is "end", the function should add the value (fourth parameter) to the end of the array and return the array.

```
function arrayManipulation(arr, command, location, val){
	if (command == "add"){
		if(location == "beginning"){
			arr.unshift(val);
			return arr;


		}else if(location == "end"){
			arr.push(val);
			return arr;
		}


	}else if (command == "remove"){
		if(location == "beginning"){
			return arr.shift(val);
			
		}else if(location == "end"){
			return arr.pop(val);
		}
		

	}
	
```

### isPalindrome

A Palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward. This function should take in one parameter and returns true or false if it is a palindrome. As a bonus, allow your function to ignore whitespace and capitalization so that isPalindrome('a man a plan a canal Panama'); returns true

```

function isPalindrome(string){
	string = string.split(" ");
	string = string.join('');
	
	for (var i = 0; i < string.length; i++){
		
		if (string[i] != string[string.length-(i+1)]){
			return false;
		}


	}
	return true;

}
```
### rockPaperScissors

Using your knowledge so far, build a game of Rock/Paper/Scissor where through the use of the prompt function, a user can enter their choice and based on a random selection - they can either tie/win or lose against a computer.

```
function rpsGame(){
      var playerHand = prompt("What will you draw (rock, paper, or scissors)? ");
      var computerHand = Math.random()
      
      if ((computerHand > 0) && (computerHand < 0.30)){
          computerHand = "rock"
      } else if ((computerHand >= 0.30) && (computerHand <0.60)){
          computerHand = "paper";
      } else{
          computerHand = "scissors";
      }
      
      if ((playerHand == "rock") && (computerHand == "scissors")){
        return "You won. Rock beats scissors!";
      } else if ((playerHand == "paper" ) && (computerHand == "rock")){
        return "You won. Paper beats rock!";
      } else if ((playerHand == "scissors") && (computerHand == "paper")){
        return "You won. Scissors beats paper!";
      } else {
          return "You lost. The " + computerHand + " beats " + playerHand;
      }
}
```

## Debugging Exercises

Answer the following questions:

What does the throw keyword do?
>Throw keyword is used to return an error. It is used to call an error object and/or set a string to get a message for that error.

What does the finally keyword do? 
>Finally is a block of code in error handling in which it will execute no matter what happens.

What is the difference between a TypeError and ReferenceError? TypeError
>Type error happens when we invoke a function or something with incorrect data type while Reference error happens when we invoke or access something outside of its scope.

How do you create a snippet in the Chrome dev tools?

>You can create at snippet by opening the developer console first. Under the Sources tab, click snippet.

In the Chrome dev tools, on the right hand side of the sources tab, there is a "pause" button which allows you to "pause on caught exceptions." What is an exception?

>Exception is an error that is found in your code. You handle errors with a try-catch code block.

How do we "catch" errors in JavaScript? Give an example with code for what that might look like.

>We catch error with the us of try-catch block.
```
try {
  var numError = 6/0;
}
catch (e) {
  console.log("The number that you define is not a valid number.");
}
```

Explain what type of error will be thrown, why the error is occuring, and how to fix it:
1. person;

The error will be a refernce error. We can fix this by declaring and initializing the variable person.

2. 
```
var data = {};
data.displayInfo();
```

The error will be a type error because we're accessing a function displayInfo. We can fix this by changing displayInfo as key and not as a function.

3.
```
var data = {};
data.displayInfo.foo = "bar";
```

The error will be a type error because we're accessing a property of an undefined function.

4.
function data(){
    var thing = "foo";
}
data();
thing; //This will be a reference error because it's accessing a variable outside of its scope.

Part 2
Fix the broken code and explain what was wrong:
1.
```
for(var i=0; i > 5; i++){
    console.log(i);
}
```

The condition for the for loop is not correct. The variable counter 'i' never satisfies the condition so the condition will be false immediately.

Fix:
```
for(var i=0; i < 5; i++){
    console.log(i);
}
```


2.
```
function addIfEven(num){
    if(num % 2 = 0){
        return num + 5;
    }
    return num;
}

```
There is a syntax error. The asignment operator "=" should be reaplaced with an equality operator "==".
```
function addIfEven(num){
    if(num % 2 == 0){
        return num + 5;
    }
    return num;
}
```

3.
```
function loopToFive(){
    for(var i=0, i < 5, i++){
        console.log(i);
    }
}
```

There is a syntax error. The comma "," should be replaced by semi-colon ";".

```
function loopToFive(){
    for(var i=0; i < 5; i++){
        console.log(i);
    }
}
```

4.
```
function displayEvenNumbers(){
    var numbers = [1,2,3,4,5,6,7,8];
    var evenNumbers = [];
    for(var i=0; i<numbers.length-1; i++;){
        if(numbers % 2 = 0); {
            evenNumbers.push(i);
        }
        return evenNumbers;
    }
}
displayEvenNumbers();
```

Syntax errors here. 
 1.) semi-colon after i++
 2.) assignment operator instead of equalit operator in the condition of the if-statement.
 3.) semi-clon after the condition in the if-statement.
 
4.) There parameter in the .push method should be numbers[i] instead of "i" only.
5.) The numbers in the if conditional statement should be numbers[i]
6.) The numbers.length-1 should only be numbers.length
7.) return evenNumbers should be outside the for loop not inside.
8.) comma inside the for loop instead of semi-colon.

```
function displayEvenNumbers(){
    var numbers = [1,2,3,4,5,6,7,8];
    var evenNumbers = [];
    for(var i=0; i<numbers.length; i++){
        if(numbers[i] % 2 == 0) {
            evenNumbers.push(numbers[i]);
        }
    }

    return evenNumbers;
}
displayEvenNumbers();
```
