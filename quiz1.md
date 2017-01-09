#Quiz 1

1. An angular directive is:
  1. The same thing as a Controller
  2. A way to define a custom element or attribute.
  3. A way to use ng-app
  4. A way for angular to communicate with a specific API

//Answer
2

2. Write the JavaScript code necessary to create a controller named "PageController" which prints the string "hello world" as soon as the page loads and the controller runs.

//Answer

angular.module("myAPP" , [])
.controller("PageController" , ["$scope" , function($scope){
  console.log("hello world");
}]);


3. Given the following angular module declaration:

  ```JavaScript
  var app = angular.module("CookiesApp", ['ngRoute', 'ngAnimate']);
  ```
  How do you bind this angular module to a p  articular portion of your html page (for instance the body tag)?

  //Answer
  <body ng-app="CookiesApp"></body>

4. Run Euclid’s GCD algorithm for the following pairs of numbers. Show work.
  1.	10, 99
  2.	12, 128
  3.	65536, 1024
  4.	24, 40
  5.	58, 57
  6.	32, 48
  7.	44, 121

//Answer

  function MCD(num1, num2){
    var smaller = Math.min(num1, num2);
    var bigger = Math.max(num1, num2);

    if(bigger % smaller == 0 ) return smaller;

    return MCD(bigger - smaller , smaller);

  }

  1.	10, 99 - 1
  2.	12, 128 - 4
  3.	65536, 1024 - 1024
  4.	24, 40 - 8
  5.	58, 57 - 1
  6.	32, 48 - 16
  7.	44, 121 - 11



5.	Given two temperatures, return true if one is less than 0 and the other is greater than 100.
  a.	icyHot(120, -1) → true
  b.	icyHot(-1, 120) → true
  c.	icyHot(2, 120) → false

//Answer
  function icyHot(temp1 , temp2){
      return temp1*temp2 < 0 && (temp1 > 100 || temp2 > 100 );
  }

6.	Given 2 ints, a and b, return true if one if them is 10 or if their sum is 10.
  a.	makes10(9, 10) → true
  b.	makes10(9, 9) → false
  c.	makes10(1, 9) → true

//Answer
  function makes10(num1 , num2){
    return num1+num2 == 10 || num1 == 10 || num2 == 10;
  }

7.	Given a string, take the first 2 chars and return the string with the 2 chars added at both the front and back, so "kitten" yields"kikittenki". If the string length is less than 2, use whatever chars are there.
  a.	front22("kitten") → "kikittenki"
  b.	front22("Ha") → "HaHaHa"
  c.	front22("abc") → "ababcab"

  function front22(word){
    if(word.length == 1) return word;

    return word.slice(0,2) + word + word.slice(0,2);
  }

8. Solve https://codility.com/programmers/lessons/3-time_complexity/frog_jmp/
  Submit the screenshot of your solution after being put through the codility grader.

9. Solve https://codility.com/programmers/lessons/3-time_complexity/tape_equilibrium/
  Submit a screenshot of your solution after being put through the codility grader.
