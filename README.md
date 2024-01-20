//Date Formatter
Working with dates in JavaScript can be challenging. You have to navigate various methods, formats, and time zones.
In this project, you'll learn how to work with the JavaScript Date object, including its methods and properties.
You'll also learn how to correctly format dates.

This project will cover concepts such as the getDate(), getMonth(), and getFullYear() methods.

// Step 1
In this project, you will learn about the JavaScript Date object by building a date formatter.

All the HTML and CSS for this project have been provided for you.

Start by getting the #current-date element using the .getElementById() method and assign it to a const variable called currentDateParagraph.

//Step 2
Use the .getElementById() method to get the #date-options element and use const to assign it to a variable named dateOptionsSelectElement.

//Step 3
In JavaScript, there are many built-in constructors that create objects.
A constructor is like a regular function, but starts with a capital letter, and is initialized with the new operator.

For example, you can use the Date() constructor with the new operator to create a new Date object that returns a string with the current date and time:

const currentDate = new Date();
console.log(currentDate);

// Output:
// Mon Aug 23 2021 15:31:00 GMT-0400 (Eastern Daylight Time)
Create a new const variable called date and assign it a Date object with new Date()

//Step 4
The Date object has a number of methods that allow you to get the date and time in different formats.

One of those is the .getDate() method, which returns a number between 1 and 31 that represents the day of the month for that date. For example:

const date = new Date();
const dayOfTheMonth = date.getDate();
console.log(dayOfTheMonth); // 20
Using const, create a variable named day and assign it the day of the month from date with the .getDate() method.

//Step 5
The .getMonth() method returns a number between 0 and 11. This represents the month for the date provided, where 0 is January and 11 is December.
Because the number this method returns is zero-based, you need to add 1 to it to get the expected month number.

Using const, create a variable named month and assign it the month from date with the .getMonth() method.

Remember to add 1 to the number returned by .getMonth().

//Step 6
The .getFullYear() method returns a number which represents the year for the provided date.

Using const, create a variable named year and assign it the year from date with the .getFullYear() method.

//Step 7
The .getHours() method returns a number between 0 and 23. This represents the hour for the provided date, where 0 is midnight and 23 is 11 p.m.

Create a const variable named hours and assign it the hour from date with the .getHours() method.

//Step 8
The .getMinutes() method returns a number between 0 and 59 which represents the minutes for the provided date.

Create a const variable named minutes and assign it the minutes from date with the .getMinutes() method.

//Step 9
Next, create a const variable named formattedDate and assign it empty template literals.

//Step 10
Inside the template literal, add an embedded expression that contains the day variable.

//Step 11
After the day variable, add a dash (-) followed by another embedded expression that contains the month variable.

//Step 12
After the month variable, add a dash followed by another embedded expression that contains the year variable.

//Step 13
To see the results of the formattedDate variable, add a console.log() statement and pass in the formattedDate variable as an argument.

Open up the console and you should see the date printed out.

//Step 14
In JavaScript, the textContent property is used to both get and set the text of a node.

For example, here's how you can get the text content from a paragraph element with the id example-paragraph, and set its text content to a new value:

<p id="example-paragraph">Example Text</p>
const exampleParagraph = document.getElementById("example-paragraph");
console.log(exampleParagraph.textContent); // "Example Text"
exampleParagraph.textContent = "New Text";
console.log(exampleParagraph.textContent); // "New Text"
Use the textContent property on currentDateParagraph to set its text content to the value of the formattedDate variable.

Also, make sure to remove your console.log(formattedDate); line.

//Step 15
In JavaScript, the change event is used to detect when the value of an HTML element has changed:

element.addEventListener("change", () => {

});
Chain the addEventListener method to dateOptionsSelectElement where the first argument is change and the second argument is an empty arrow function.

//Step 16
When a user makes a selection from the dropdown menu, the function should get the user's value and display the date in their chosen date format.
To do this, you can use the switch statement.

A switch statement is used to compare an expression against multiple possible values and execute different code blocks based on the match.
It's commonly used for branching logic.

For example, here's how to compare the expression dayOfWeek against possible values:
switch (dayOfWeek) {
case 1:
console.log("It's Monday!");
break;
case 2:
console.log("It's Tuesday!");
break;
// ...cases for other workdays
default:
console.log("It's the weekend!");
}
Create a switch statement and use dateOptionsSelectElement.value as the expression.

//Step 17
When the user chooses the Year, Month, Day option from the dropdown, the date format should reflect this choice.

To do this, you can add a case clause in the switch statement that checks for a match against the expression expr, followed by code to run if there's a match.
Here's an example where the case clause checks that expr is equal to the string case123:

switch (expr) {
case 'case123':
// Write your logic here
}
Add a case where the value is yyyy-mm-dd. Inside the case, set the text content of currentDateParagraph to the value of formattedDate.

//Step 18
Split formattedDate into an array of substrings with the .split() method and use a "-" as the separator.

//Step 19
The .reverse() method is used to reverse an array in place. For example:

const array = [1, 2, 3, 4, 5];
array.reverse();
console.log(array); // [5, 4, 3, 2, 1]
Chain the .reverse() method to the end of .split() method.

//Step 20
Finally, you need to create a string with the reversed array elements separated by dash (-) character.

Use the .join() method to join the reversed array elements into a string and use a "-" for the separator.

//Step 21
If your switch statement is going to have multiple cases, it is best practice to include a break statement.

The break statement will tell the JavaScript interpreter to stop executing statements.
Without adding a break statement at the end of each case block, the program will execute the code for all matching cases:

switch (someVariable) {
case 'case123':
// Write your logic here
break; // Terminates the switch statement
}
Add a break statement to the end of your case block.

//Step 22
Add another case with the value mm-dd-yyyy-h-mm.
Inside that case, set the text content of currentDateParagraph to empty template literals.

Also, make sure to include a break statement to terminate the switch statement.

//Step 23
Inside the case for mm-dd-yyyy-h-mm, set the textContent property of currentDateParagraph to ${month}-${day}-${year} ${hours} Hours ${minutes} Minutes.

//Step 24 -> Last Step
In a switch statement, the default case is executed when none of the previous case conditions match the value being evaluated.
It serves as a catch-all for any other possible cases. For example:
