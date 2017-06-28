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
## Exercises

1. Create an array of your favorite foods (call it favoriteFoods). Make sure it has at least three elements.

  >favoriteFoods = ["pizza", "icecream", "burger"];
	
2. Access the second element in favoriteFoods.

>favoriteFoods[2]
	
3. Change the last element in favoriteFoods to some other food.

>favoriteFoods[(favoriteFoods.length - 1)] = "spaghetti"
	
4. Remove the first element in favoriteFoods and store it in a variable called formerFavoriteFood.

>formerFavoriteFood = favoriteFoods.shift();
	
5. Add a favorite food to the back of the favoriteFoods array.

>favoriteFoods.push("wings");
	
6. Add a favorite food to the front of the favoriteFoods array.

>favoriteFoods.unshift("ham");
	
7. What happens when you try to pop from an empty array?

>Nothing is added to the array. And the function returns undefined.
    
8. In the examples below, use splice to convert the first array to the second array:
>people.slice(2);

9.  Write the command that gives the indexOf where "Foo" is located (this should return -1).
>people.indexOf("Foo");
    
10. Redefine the people variable with the value you started with. 
.Using the splice command, remove "Devon" from the array and add "Elizabeth" and "Artie". Your array should look like this when you are done ["Greg", "Mary", "Elizabeth", "Artie", "James"].

```
var people = ["Greg", "Mary", "Devon", "James"];
people.splice(2,1,"Elizabeth", "Artie");
```

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
1 Write a function called myName that logs your full name. Save your full name to a variable inside of the function body, then use console.log to print your name to the console.
```
function myName(){
  var fullName = prompt("Please enter your Full Name: ");
  return fullName

}

console.log(myName())
```
2. Create an array called favoriteFoods which contains the strings "pizza" and "ice cream".
```
var favoriteFood = ["pizza", "icecream"];
```
3. Write a function called randomFood. The function should use Math.random to randomly choose a favorite food in your favoriteFoods array to return. For example, your function will return either pizza or ice cream, depending on what you get back from Math.random.
```
function randomFood(){  
 
 var favoriteFood = ["pizza", "icecream"];
 
 return Math.random() > .5 ? favoriteFood[0] : favoriteFood[1]
 
}
```
4. Create a variable called numbers which is an array that contains the numbers 1 through 10.

var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];

5. Write a function called displayOddNumbers which iterates over the numbers array and console.logs out all of the numbers that are odd.
``` 
function displayOddNumbers(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	for (i=0; i<num.length; i++){

		if ((num[i] % 2) != 0) {
		   console.log(num[i]);
		}
	}

}

displayOddNumbers();
```
6. Write a function called displayEvenNumbers which iterates over the numbers array and console.logs out all of the numbers that are even.
```
function displayEvenNumbers(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	for (i=0; i<num.length; i++){

		if ((num[i] % 2) == 0) {
		   console.log(num[i]);
		}
	}

}

displayEvenNumbers();

```
7. Create a function called returnFirstOddNumber which iterates over the numbers array and returns the first odd number it finds
```
function returnFirstOddNumber(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	for (i=0; i<num.length; i++){

		if ((num[i] % 2) != 0) {
		   return num[i];
		}
	}

}

returnFirstOddNumber();
```

8. Create a function called returnFirstEvenNumber which iterates over the numbers array and returns the first even number it finds
```
function returnFirstEvenNumber(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	for (i=0; i<num.length; i++){

		if ((num[i] % 2) == 0) {
		   return num[i];
		}
	}

}

returnFirstEvenNumber();
```
9. Create a function called returnFirstHalf which returns the first half of the numbers array
```
function returnFirstHalf(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	return num.slice(0, 5);

}

returnFirstHalf();
```
10. Create a function called returnSecondHalf which returns the second half of the numbers array
```
function returnSecondHalf(){
	var num = [1, 2, 3, 4, 5, 6, 7 , 8, 9 , 10];
	
	return num.slice(5);

}
returnSecondHalf();
```
