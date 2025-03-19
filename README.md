# Javascript

// How to Declare a Varibale :
var CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_;

//How to take input from User using => prompt();
CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ = prompt("What is your name ?");

//How to show screen-popup output using => alert();
alert("your's name is "+ CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ );

//data type of a variable => typeof(myVar);

//length of a string => myVar.length;

//substring of a string => myVar.slice(0,2); => From 0th Position to upto, but including 2nd Position.

//change sting to Upper Case => myVar.toUpperCase();

//change sting to Lower Case => myVar.toLowerCase();

// Division "/" gives Output as "number" (not float) and Modulo "%" also gives "number"
alert("data-type of division is a : " + typeof(5/2) + "( not float), while of a Modulo is : " + typeof(4%2) )

// y = x++; => x value will assign first to y before x is incremented.
// y += 1 => y will be incremented by 1 and then again assigned to y.

//To print something in developer-console => console.log("myVar is :" + myVar)

//We can use some Math functions like Math.floor(), Math.ceil(), Math.round(),Math.PI etc. 

//function-declaration don't have semi-colon in end
function add (a,b){
    return a + b;
}

// function-calling have a semi-colon in end
add(2,3);
