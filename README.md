# BOOLEAN LOGIC EXERCISES

# Part 1
Write down what the following statements will return. Try to figure this out before putting the commands in the chrome console.


Answers:

	1.) 2 == "2";
	true
	2.) 2 === 2;
	true
	3.) 10 % 3;
	true
	4.) 10 % 3 === 1;
	true
	5.) true && false;
	false
	6.) false || true;
	true
	7.) true || false;
	true

Part II
Answer the following questions about this code block:
1. The code should print "Keep it up!"
2. We do not need to specify it because condition in if-else statements will be forced into a boolean. It works on its own because isLearning value is true;

1. It should console log "third" because it is the first conditional statement to satisfy its condition.
2. undefined
3. It's not a truthy value because it has a value of undefined and undefined is a falsy value.
4. The secondVariable is not a truthy value because single quotes and double quotes are considered as falsy value.
5. The value of the thirdVariable is a truthy value because 1 is considered as true.

Part III
1.

if (Math.random() < 0.5){
	console.log "Over 0.5";
} else{
	console.log "Under 0.5";
}

2. 
List of falsy Values:
false 
0 and -0
NaN
null
undefined
"" and ''






ARRAY EXERCISES
Exercises
1. Create an array of your favorite foods (call it favoriteFoods). Make sure it has at least three elements.
	favoriteFoods = ["pizza", "icecream", "burger"];
2. Access the second element in favoriteFoods.
	favoriteFoods[2]
3. Change the last element in favoriteFoods to some other food.
	favoriteFoods[(favoriteFoods.length - 1)] = "spaghetti"
4. Remove the first element in favoriteFoods and store it in a variable called formerFavoriteFood.
	formerFavoriteFood = favoriteFoods.shift();
5. Add a favorite food to the back of the favoriteFoods array.
	favoriteFoods.push("wings");
6. Add a favorite food to the front of the favoriteFoods array.
	favoriteFoods.unshift("ham");
7. What happens when you try to pop from an empty array?
    Nothing is added to the array. And the function returns undefined.
8. In the examples below, use splice to convert the first array to the second array:
  
9.  Write the command that gives the indexOf where "Foo" is located (this should return -1).
    
10. Redefine the people variable with the value you started with. Using the splice command, remove "Devon" from the array and add "Elizabeth" and "Artie". Your array should look like this when you are done ["Greg", "Mary", "Elizabeth", "Artie", "James"].
