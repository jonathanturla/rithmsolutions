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
## Exercises
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

## isPalindrome

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
