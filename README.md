# Solved-Tasks
#### Do I get a bonus?
```javascript
function bonusTime(salary, bonus) {
if (bonus == true){
  salary *= 10;
  return "\u00A3"+salary;
  }else{
    return "\u00A3"+salary;
  }
}
```
#### Generate range of integers
```javascript
function generateRange(min, max, step){
let array = [];
for (let i = min;i <=max; i+=step){
  array.push(i);
  }
  return array;
}
```
#### CodeWars Task : Keep up the hoop
```javascript
function hoopCount (n) {
   if (n >= 10){
   return "Great, now move on to tricks";
   } else {
   return "Keep at it until you get it";  
   }
}
```
#### CodeWars Task :Alan Partridge II - Apple Turnover
```javascript
function apple(x){
  return (Math.pow(x,2) > 1000) ?  'It\'s hotter than the sun!!' : 'Help yourself to a honeycomb Yorkie for the glovebox.';
}
```
#### CodeWars Task :Count of positives / sum of negatives
```javascript
function countPositivesSumNegatives(arr) {
    if (arr === null || arr.length === 0) return [];
    
    let countPos = 0, summNeg = 0;
    
    for (let i = 0;i < arr.length; i++){
    if (arr[i] > 0){
    countPos++;
    } else {
    summNeg +=arr[i];
    }
   }
   return [countPos,summNeg];
}
```
#### CodeWars Task :I love you, a little , a lot, passionately ... not at all
```javascript
function howMuchILoveYou(n) {
    const fl = ['I love you','a little','a lot','passionately','madly','not at all'];
return fl[(n - 1) % 6];

}
```
#### CodeWars Task : Complementary DNA
```javascript

function DNAStrand(dna){
  let a = '';
  
  for (let i = 0; i < dna.length; i++){
    if (dna[i] === 'A') a+= 'T';
    if (dna[i] === 'T') a+= 'A';
    if (dna[i] === 'G') a+= 'C';
    if (dna[i] === 'C') a+= 'G';
  }
  return a;
}
```
#### CodeWars Task : Sum of differences in array
```javascript
function sumOfDifferences(arr) {
const sorted = arr.sort((a,b) => b-a);
let summ = 0;

for (let i = 0;i < sorted.length - 1; i++){
  summ += sorted[i] - sorted[i + 1];

  }

return summ;
}
```
#### CodeWars Task : Draw stairs
```javascript
function drawStairs(n) {
  
  let s = '';
  for (let i = 1; i<=n ; i++){
  s += i === n ? 'I' :'I\n' + ' '.repeat(i)
  }
    return s;
}
```
#### CodeWars Task : A wolf in sheep's clothing
```javascript
function warnTheSheep(q) {
const l = q.length;
const w = q.indexOf('wolf');
if (l === w + 1) return "Pls go away and stop eating my sheep";

return `Oi! Sheep number ${l - 1 - w}! You are about to be eaten by a wolf!`;
}
```
#### CodeWars Task : Sum ALL the arrays!
```javascript
function arraySum(arr) {
let a = arr.toString().split(',');
let sum = 0;
for (let i = 0;i < a.length; i++){
  sum+= Number.isNaN(Number (a[i])) ? 0 : Number (a[i]);
  }
  return sum;
}
```
#### CodeWars Task : Remove duplicates from list
```javascript
function distinct(a) {

  let b ={};
  let res = [];
  for (let i = 0; i < a.length; i++){
  if(!b[a[i]]){
  res.push(a[i]);
  b[a[i]] = 1;
  
  }
  }
  return res;
}
```
#### CodeWars Task : sPoNgEbOb MeMe
```javascript
function spongeMeme(sen) {
  let bob = '';
  for (let i = 0; i < sen.length; i++){
  if (i % 2 !== 0){
   bob += sen[i].toLowerCase();
   } else {
   bob += sen[i].toUpperCase();
   }
  }
  return bob;
}
```
#### CodeWars Task : Area of a Square
```javascript
function squareArea(A){
  return Math.round(Math.pow( (A / (2 * Math.PI)) * 4   , 2 ) * 100 ) / 100;
}
```
#### CodeWars Task : Calculate BMI
```javascript
function bmi(weight, height) {
  let bmi = weight / (height ** 2);
  console.log(bmi);
  if (bmi <= 18.5){
  return "Underweight";
  } else if (bmi <= 25.0 ){
  return "Normal";
  } else if (bmi <= 30.0 ){
  return "Overweight";
  } else {
  return "Obese";
  }
}
```
#### CodeWars Task : What's the real floor?
```javascript
function getRealFloor(n) {
 console.log(n)
 if (n <= 0){
  return n;
  } else if (n >= 1 && n < 14  ){
  return n - 1;
  }else {
  return n - 2;
  }
}
```
#### CodeWars Task : Calculate Two People's Individual Ages
```javascript
function getAges(s,d){
  console.log(s,d)
  if (s < 0 || d < 0 || d > s){
  return null;
  } else {
  return [(s + d) / 2 , ((s + d) / 2) - d] ;
  }
  
}
```
#### CodeWars Task : 101 Dalmatians - squash the bugs, not the dogs!
```javascript
function howManyDalmatians(number){
  
  var dogs = ["Hardly any", "More than a handful!", "Woah that's a lot of dogs!", "101 DALMATIANS!!!"];
  
  var respond = (number <= 10) ? dogs[0] : (number <= 50) ? dogs[1] : (number === 101)?  dogs[3] : dogs[2];
  
return respond;
}
```
#### CodeWars Task : Odd or Even?
```javascript
function oddOrEven(array) {
     let sum = 0;
     for (let i = 0; i < array.length;i++){
     sum += array[i];
     }
     return sum % 2 ? 'odd' : 'even';
}
```
#### CodeWars Task : Difference Of Squares
```javascript
function differenceOfSquares(n){
  let sum = 0;
  let sumSquares = 0;
  while (n > 0){
    sum += n;
    sumSquares += Math.pow(n , 2);
    n--;
  }
  let squareSum = Math.pow(sum, 2)
  
  
  return squareSum - sumSquares;
}
```
#### CodeWars Task : Powers of 3
```javascript
function largestPower(n){
  let k = 0;
  while (Math.pow(3,k) < n){
  k++;
  }
  
  return k-1;
}
```
#### CodeWars Task : Sum of the first nth term of Series
```javascript
function SeriesSum(n){
  let result = 1;
  let sum = 1;
 if (n === 0 || n ===1 ){
   return n.toFixed(2); 
   } else {
     for (i = 1; i < n; i++){
       sum +=3;
       result +=(1/sum)
       }
    }
    
   return result.toFixed(2)
}
```
#### CodeWars Task : Beginner Series #3 Sum of Numbers
```javascript
function getSum( a,b ){
 console.log(a, b)
 let sum = 0;
  if (a < b){
    for (let i = a; i <= b; i++){
      sum += i;   
    }
  } else {
    for (let i = b; i <= a; i++){
      sum += i;   
    }
  }
  return sum;
}
```
#### CodeWars Task : Power
```javascript
function numberToPower(n, p){
  console.log(n,p)
  let iGotPower = 1;
  let number = p;
  if (p == 0){
   return iGotPower;
  } else {
    do {
      iGotPower *= n;
    number--;
    }  
  while (number > 0);
  }
  return iGotPower;
}
```
#### CodeWars Task : Filter the number
```javascript
var FilterString = function(value) {
  let string = "";
  for (i = 0;i < value.length; i++){
    if (isNaN(value[i])){
      continue;
      
    } else {
      string += value[i];
    }
  }
  return +string;
}
```
#### CodeWars Task : Squares sequence
```javascript
function squares(x, n) {

 let arr = [];
  let mult = x;
  for (let i = 0;i < n; i++ ){
    arr[i] = mult;
    mult *= mult;
   
    }

return arr;
}
```
#### CodeWars Task : Square Every Digit
```javascript
function squareDigits(num){
  let str = num + "";
  let strNum = "";
  for (let i = 0 ; i < str.length; i++){
    strNum += Math.pow(str[i], 2);
  }
  return +strNum;
}
```
#### CodeWars Task : Find the next perfect square!
```javascript
function findNextSquare(sq) {
  let notPerfect = -1;
  if (Math.sqrt(sq) % 1 == 0){
    return Math.pow(Math.sqrt(sq) + 1, 2);
  } else {
  return notPerfect;
  }
}
```
#### CodeWars Task : The wheat/rice and chessboard problem
```javascript
function squaresNeeded(g){
  if (g == 0){
  return 0;
  } else {
    return 1 + Math.trunc(Math.log2(g));
  }
}
```
#### CodeWars Task : Tortoise racing
```javascript
function race(v1, v2, g) {
   let hours;
   let distance;
   let minutes;
   let seconds;
  if (v1 >= v2){
    return null;
  } else {
    distance = (v2 * g) / (v2 -v1);
  }
  hours = distance / v2
  minutes = (hours - Math.trunc(hours)) * 60
  seconds = ((minutes - Math.trunc(minutes))).toFixed(3) * 60
  
  return [Math.trunc(hours), Math.trunc(minutes), Math.trunc(seconds)]
  
}
```
#### CodeWars Task : Lario and Muigi Pipe Problem
```javascript
function pipeFix(numbers){
let array = [];
for (let i = Math.min(...numbers) ;i <= Math.max(...numbers); i++){
  array.push(i);
  }
  return array;
}
```
#### CodeWars Task : Calculate Price Excluding VAT
```javascript
function excludingVatPrice(price){
  let originalPrice = price - ((price * 15) / 115);
  
 if (price == null){
    return -1;
  } else {
  return +originalPrice.toFixed(2);
  }
  
}
```

#### CodeWars Task : Is every value in the array an array?
```javascript
const arrCheck = value =>{
  if (value.length == 0) return true;
  for (let i = 0; i < value.length; i++){
    if ({}.toString.call(value[i]) != "[object Array]" ){
      return false;
    } else if ({}.toString.call(value[value.length - 1]) == "[object Array]" ){
      return true;
    }
  }  
}
```

#### CodeWars Task : A Needle in the Haystack
```javascript
function findNeedle(haystack) {
  let position = 0;
  for (let i = 0; i < haystack.length ; i++){
    if (haystack[i] === 'needle' ){
      position = i;
      break;
    }
  }
  return `found the needle at position ${position}`;
}
```
#### CodeWars Task : Sum of positive
```javascript
function positiveSum(arr) {
  let sumPositive = 0;
  for (let i = 0; i < arr.length; i++){
    if (arr[i] > 0){
      sumPositive += arr[i];
    }
  }
  return sumPositive;
}
```
#### CodeWars Task : Divide and Conquer
```javascript
function divCon(x){
  let sumNumbers = 0;
  let sumStrings = 0;
  for (let i = 0; i < x.length; i++){
    if (typeof x[i] == 'string'){
      sumStrings += +x[i]; 
    } else {
      sumNumbers += x[i];
    }
  }
  return sumNumbers - sumStrings;
}
```
#### CodeWars Task : Sum of Odd Cubed Numbers
```javascript
function cubeOdd(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i ++){
    if (typeof arr[i] == 'string'){
      return undefined;
      
    } else if (arr[i] % 2 !== 0) {
      sum += Math.pow(arr[i], 3);  
    }
  }

  return sum;
}
```
#### CodeWars Task : Sum of two lowest positive integers
```javascript
function sumTwoSmallestNumbers(numbers) {  
  let minOne = Math.min(...numbers);
  numbers.splice(numbers.indexOf(Math.min(...numbers)),1);
  let minTwo = Math.min(...numbers);
  return minOne + minTwo;
}
```
#### CodeWars Task : Remove the minimum
```javascript
function removeSmallest(numbers) {
  let myArray = [...numbers];
  myArray.splice(myArray.indexOf(Math.min(...myArray)),1)
  console.log(numbers);
 return myArray;

}
```
#### CodeWars Task : Sum without highest and lowest number
```javascript
function sumArray(array) {
  let sum = 0;
  if (array == null || array.length < 3 ){
    return 0;
  } else {   
    array.splice(array.indexOf(Math.min(...array)),1);
    array.splice(array.indexOf(Math.max(...array)),1);
    for (let i = 0 ; i < array.length;i++){
    sum += array[i];
    }
  }  
  return sum;
}

```
#### CodeWars Task : Find the divisors!
```javascript
function divisors(integer) {
  let count = 0;
  let arr = [];
 console.log(integer)
  for (let i = 2; i < integer; i++){
    if (integer % i == 0){
      arr.push(i);
      count++;
    }
  }
  if (count == 0){
    return `${integer} is prime`
  } else {
    return arr;
  }
}
```
#### CodeWars Task : JavaScript Array Filter
```javascript
function getEvenNumbers(numbersArray){
 return numbersArray.filter(function(numbers){
   return numbers % 2 == 0;
 });
}
```
#### CodeWars Task : Find how many times did a team from a given country win the Champions League?
```javascript
function countWins(winnerList, country) {
  let myList = winnerList.filter(el => el.country == country);
  return myList.length;
}
```
#### CodeWars Task : filterEvenLengthWords
```javascript
function filterEvenLengthWords(words) {
  return words.filter(word => word.length % 2 == 0);
}
```
#### CodeWars Task : Santa's Naughty List
```javascript
function findChildren(santasList, children) {
  let myList = [];
  for (let i = 0; i < children.length; i++){
    if (santasList.includes(children[i])){
      myList.push(children[i]);
    } 
  }
 return myList.filter((el,i) => myList.indexOf(el) === i).sort();
}
```
#### CodeWars Task : Array.diff
```javascript
function array_diff(a, b) {
 console.log(a, b)
 return a.filter( ( el ) => !b.includes( el ) );
}
```
#### CodeWars Task : Find Duplicates
```javascript
function duplicates(arr) {
  return arr.filter((el, i) => i !== arr.indexOf(el) && i === arr.lastIndexOf(el));
}
```
#### CodeWars Task : Train to remove duplicates from an array with filter()
```javascript
function unique(arr) {
  return arr.filter((el, i) => i === arr.indexOf(el));
}
```
#### CodeWars Task : Two Oldest Ages
```javascript
function twoOldestAges(ages){
  ages.sort((a, b) => a - b);
  return [ages[ages.length - 2], ages[ages.length - 1] ]; 
}
```
#### CodeWars Task : String Templates - Bug Fixing #5
```javascript
function buildString(...template){
  return `I like ${template.join(', ')}!`;
}
```
#### CodeWars Task : Regex validate PIN code
```javascript
function validatePIN (pin) {
    for ( let i = 0;i < pin.length; i++){
      if (pin.codePointAt(i) > 47 && pin.codePointAt(i) < 58 ){
        continue;
      } else {
        return false;
      }
    }
  if (pin.length == 4 || pin.length == 6){
    return true;
  } else {
    return false;
  } 
}
```
#### CodeWars Task : Numbers to Letters
```javascript
function switcher(x){
 let string = '';
 let letters = ["z", "y", "x", "w", "v", "u", "t", "s", "r", "q","p", "o", "n", "m", "l", "k", "j", "i", "h", "g","f", "e", "d", "c", "b", "a","!","?"," "];
 for (let i = 0; i < x.length; i++){
   string += letters[+x[i]-1];
 }
 return string;
}
```
#### CodeWars Task : Unique In Order
```javascript
var uniqueInOrder=function(iterable){

  let myArray = [];
  for (let i = 0;i < iterable.length;i++){
    if (myArray[myArray.length -1]  !== iterable[i] ){
      myArray.push(iterable[i]);
    }  
  }
  console.log(iterable,myArray)
  return myArray;
}
```
#### CodeWars Task : Thinking & Testing : Something capitalized
```javascript
function testit(s){
  if (s.length == 0)  return s; 
  let testSomething = s.split(" ")
  for (let i = 0; i < testSomething.length ;i++){
    testSomething[i] = testSomething[i].slice(0,-1) + testSomething[i][testSomething[i].length -1].toUpperCase(); 
  }
  return testSomething.join(" ");
}
```
#### CodeWars Task : Mumbling
```javascript
function accum(s) {
	let arr = s.toLowerCase().split("");
  for (let i = 0; i < arr.length; i++){
    arr[i] = arr[i].toUpperCase() + arr[i].repeat(i); 
  }
  return arr.join("-");
}
```
#### CodeWars Task : Find the capitals
```javascript
var capitals = function (word) {
	let arr = [];
  for (let i = 0;i < word.length;i++){
    if (word[i] === word[i].toUpperCase()){
      arr.push(word.indexOf(word[i]))
    }
  }
  return arr;
};
```
#### CodeWars Task : Don't give me five!
```javascript
function dontGiveMeFive(start, end) {
  var noFive = 0;
  for (i = start; i <= end; i++) {
    if (i.toString().includes("5")){
      continue;
    } else {
      noFive++;
    }
  }
  return noFive;
}
```
#### CodeWars Task : String ends with?
```javascript
function solution(str, ending){
  return str.endsWith(ending);
}
```
#### CodeWars Task : Tail Swap
```javascript
function tailSwap(arr) {
  let myArr = [];
  myArr[0] = arr[0].slice(0,arr[0].indexOf(':')) + arr[1].slice(arr[1].indexOf(':'));
  myArr[1] = arr[1].slice(0,arr[1].indexOf(':')) + arr[0].slice(arr[0].indexOf(':'));
  return myArr;
}
```
#### CodeWars Task : Credit Card Mask
```javascript
function maskify(cc) {
  if (cc.length < 5) return cc;
  return "#".repeat(cc.length -4) + cc.slice(-4);
}
```
#### CodeWars Task : Squash the bugs
```javascript
function findLongest(str){
  
  var spl = str.split(" ");
  var longest = 0;
  
  for (var i = 0; i < spl.length; i++){
    if (spl[i].length > longest) {
      longest = spl[i].length;
    }
  }
    return longest;
}
```
#### CodeWars Task : Descending Order
```javascript
function descendingOrder(n){
  let m = n.toString().split("").sort((a,b) => b - a).join("");
  return +m;
}
```
#### CodeWars Task : Highest and Lowest
```javascript
function highAndLow(numbers){
  let num = numbers.split(" ").sort((a,b) => b - a);
  return num[0] + " " + num[num.length -1]
}
```
#### CodeWars Task : Can Santa save Christmas?
```javascript
function determineTime(durations){
  if (durations.length == 0) return true;
  let sec = 0;
  let min = 0;
  let hours = 0;
  for (let i = 0; i < durations.length;i++){
    sec += + (durations[i][6] + durations[i][7]);
    min += + (durations[i][3] + durations[i][4]);
    hours += + (durations[i][0] + durations[i][1]);
  }
  min += Math.trunc(sec / 60);
  hours += Math.trunc(sec / 60);
  return hours < 24;
}
```
#### CodeWars Task : Every possible sum of two digits
```javascript
function digits(num){
  let arr = num.toString().split("");
  let myArr = [];
  for (let i = 0; i < arr.length ; i++){
    for(let k = 1+i; k < arr.length; k++){
      myArr.push(+arr[i]+ +arr[k]);
    }
  }
  return myArr;
}
```
#### CodeWars Task : Duck Duck Goose
```javascript
function duckDuckGoose(players, goose) {
  if (goose <= players.length) return players[goose - 1].name;
  if (goose % players.length == 0){
    return players[players.length - 1].name;
  } else {
    return players[(goose % players.length) - 1].name;
  }  
}
```
#### CodeWars Task : Welcome!
```javascript
function greet(language) {
  let greeting = {
    english: 'Welcome',
    czech: 'Vitejte',
    danish: 'Velkomst',
    dutch: 'Welkom',
    estonian: 'Tere tulemast',
    finnish: 'Tervetuloa',
    flemish: 'Welgekomen',
    french: 'Bienvenue',
    german: 'Willkommen',
    irish: 'Failte',
    italian: 'Benvenuto',
    latvian: 'Gaidits',
    lithuanian: 'Laukiamas',
    polish: 'Witamy',
    spanish: 'Bienvenido',
    swedish: 'Valkommen',
    welsh: 'Croeso',
  } 
  return language in greeting ? greeting[language] : greeting.english;
}
```
#### CodeWars Task : Make a function that does arithmetic!
```javascript
function arithmetic(a, b, operator){
  switch(operator) {
    case 'add':  
    return a + b;
    break;

    case 'subtract':
    return a - b;
    break;
    case 'multiply':
    return a * b;
    break;
    case 'divide':
    return a / b;
    break;
  }
}
```
#### CodeWars Task : makeBackronym
```javascript
let makeBackronym = function(string){
  let arr = string.toUpperCase().split("");
  let phrase = "";
  for (let i = 0; i < arr.length ; i++){
    if (i == arr.length - 1){
      phrase += dict[arr[i]];
    } else {
      phrase += dict[arr[i]] + " ";
    }
  }
   return phrase;
};
```
#### CodeWars Task : Check three and two
```javascript
function checkThreeAndTwo(array) {
  let countA = 0;
  let countB = 0;
  let countC = 0;
  for ( let i = 0; i < array.length; i++){
    if ( array[i] == 'a') countA++;
    if ( array[i] == 'b') countB++;
    if ( array[i] == 'c') countC++;
  }
  return ((countA == 3 || countB == 3 || countC == 3) && (countA == 2 || countB == 2 || countC == 2));
}
```
#### CodeWars Task : Job Matching #1
```javascript
function match(candidate, job) {
  if (candidate.minSalary === undefined || job.maxSalary === undefined ) throw "Error";
  return candidate.minSalary - candidate.minSalary / 10 <= job.maxSalary;
}
```
#### CodeWars Task : Add property to every object in array
```
for ( let i = 0; i < questions.length ; i++){
  questions[i].usersAnswer = null;
} 
```
#### CodeWars Task : Numbers to Objects
```javascript
function numObj(s){
  let obj = [];
  for( let i = 0; i < s.length; i++){
    obj[i] = {};
    obj[i][s[i]] = String.fromCharCode(s[i]);
  }
  return obj;
}
```
#### CodeWars Task : Coding Meetup #5 - Higher-Order Functions Series - Prepare the count of languages
```javascript
function countLanguages(list) {
 let answer = {};
  for (i = 0; i< list.length; i++){
    if (answer[list[i].language]) {
      answer[list[i].language]++;
    } else {
      answer[list[i].language] = 1;
    }
  }
  return answer;
}
```
#### CodeWars Task : The Office I - Outed
```javascript
function outed(meet, boss){
  let sumMood = 0;
  let count = 0;
  for (let e in meet){
    if(e === boss ){
      sumMood += meet[e] * 2
      count++
    } else {
      sumMood += meet[e];
      count++;
    }  
  }
 return (sumMood / count) <= 5 ? 'Get Out Now!' : 'Nice Work Champ!';
}
```
#### CodeWars Task : How many days are we represented in a foreign country?
 ```javascript
function daysRepresented(trips){
  let days = [];
  for ( let i = 0; i < trips.length; i++){
    for (let k = trips[i][0]; k <= trips[i][1]; k++){
      if (!days.includes(k)){
        days.push(k);
      }
    }
  }
  return days.length;
}
```
#### CodeWars Task : What is my name score? #1
```javascript
function nameScore(name){
  let score = {};
  score[name] = 0
  let arr = name.toUpperCase().split("");
  for (let i = 0; i < arr.length; i++){
    for ( let key in alpha){
      if (key.includes(arr[i])){
        score[name] += alpha[key];
        console.log(name)
      }
    }
  }
  
  return score;
}
```
#### CodeWars Task : Permute a Palindrome
```javascript
function permuteAPalindrome (input) { 
  let countOdd = 0;
  let arr = input.split("");
  let obj = {};
  for ( let i = 0; i < arr.length; i++ ){
    if ( arr[i] in obj){
      obj[arr[i]]++;
    } else {
      obj[arr[i]] = 1;
    }
  }
  for (let key in obj){
    if (obj[key] % 2 != 0){
      countOdd++;
    }
  }
  return countOdd <= 1;  
}
```
#### CodeWars Task : Most valuable character
```javascript
function solve(st) {
  let obj = {};
  for (let i = 0; i < st.length; i++) {
    obj[st[i]] = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
  }
  let arr = [];
  for (let key in obj){
    arr.push(obj[key]);
  }
  
  let value = Math.max(...arr);
  let arrWithEqualValue = [];
  for (let key in obj){
    if (obj[key] === value) arrWithEqualValue.push(key);
  }
  arrWithEqualValue.sort();
  return arrWithEqualValue[0];
}
```
#### CodeWars Task : The Office II - Boredom Score
```javascript
function boredom(staff){
  let staffScores = {
    accounts : 1,
    finance:  2,
    canteen : 10,
    regulation : 3,
    trading : 6,
    change : 6,
    IS : 8,
    retail : 5,
    cleaning : 4,
   'pissing about' : 25,
  };
  let score = 0;
  for (let key in staffScores) {
    for (let keys in staff){
    if (key === staff[keys]) score += staffScores[key]; 
  }
  }
  if (score <= 80) {
    return 'kill me now';
  } else if (score < 100 && score > 80) {
    return 'i can handle this';
  } else {
    return 'party time!!';}
}
```
#### CodeWars Task : Who likes it?
```javascript
function likes(names) {
  if (names.length == 0) return "no one likes this";
  if (names.length == 1) return `${names[0]} likes this`;
  if (names.length == 2) return `${names[0]} and ${names[1]} like this`;
  if (names.length == 3) return `${names[0]}, ${names[1]} and ${names[2]} like this`;
  if (names.length > 3) return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
}
```
#### CodeWars Task : Valid Parentheses
```javascript
function validParentheses(str){
let a = 0;
for ( let i = 0; i < str.length ; i++){
  if (str[i] === '(') a = a + 1;
  else if (str[i] === ')') a = a - 1;
  if (a < 0) return false;
}
  return (a === 0);
}
```
#### CodeWars Task : String Reordering
```javascript
function sentence(List) {
  let arr = []
  let str = "";

  for (let i = 0; i < List.length; i++){
    arr = arr.concat(Object.keys(List[i]))
  }
  arr.sort((a, b) => a-b)

  for (let k = 0; k < List.length; k++){
    
    for(let x = 0; x < List.length; x++){
      if (arr[k] in List[x])
      { str += " " + List[x][arr[k]] }
    }
  }  
  return str.trim();
}
```
#### CodeWars Task : Print a Rectangle Using Asterisks
```javascript
function getRectangleString(w, h) {
  let rn = '\r\n';
  let tb ='*'.repeat(w) + rn;
  let center = (w > 1) ? ('*' + ' '.repeat(w - 2) + '*' + rn).repeat(h-2) : '';
  return h > 1 ? (tb + center + tb) :  tb.repeat(h);
}
```
#### CodeWars Task : Arrays Similar
```javascript
function arraysSimilar(arr1, arr2) {
  if(arr1.length !== arr2.length) return false;
  
  arr1.sort();
  arr2.sort();
  
  for( let i = 0; i < arr1.length; i++){
    if (arr1[i] !== arr2[i]) return false;
  }
  return true;
}
```
#### CodeWars Task : Write shortest function to calculate Average number of Array
```javascript
function avg(a){ return ( a.reduce((a, b) => a + b ) )/ a.length }
```
#### CodeWars Task : Get the mean of an array
```javascript
function getAverage(marks){
  return Math.floor(marks.reduce((a,b) => a + b) / marks.length)
}
```
#### CodeWars Task : Find the missing element between two arrays
```javascript
function findMissing(arr1, arr2) {
  let index;
  for(let i = 0; i < arr1.length; i++){
    index = arr2.indexOf(arr1[i]);
    if(index > -1){
      arr2.splice(index,1);
    } else {
      return arr1[i];
    }
  }

}
```
#### CodeWars Task : The Feast of Many Beasts
```javascript
function feast(beast, dish) {
  return (beast[0] === dish[0] && beast[beast.length - 1] === dish[dish.length - 1] ) 
}
```
#### CodeWars Task : Find out whether the shape is a cube
```javascript
var cubeChecker = function(volume, side){
 if (side === 0 || side < 0) return false;
  return side ** 3 === volume;
};
```
#### CodeWars Task : Multiplication table for number
```javascript
function multiTable(n) {
  let res = '';
  for (let i = 1; i <= 10; i++){
    res += `${ i } * ${ n } = ${ i * n }${i < 10 ? '\n' : ''}`;
  }
  return res;
}
```
#### CodeWars Task : Get Nth Even Number
```javascript
function nthEven(n){
  return n * 2 - 2;
}
```
#### CodeWars Task : Enumerable Magic #2 - True for Any?
```javascript
function any(arr, fun){
  return arr.some(fun);
}
```
#### CodeWars Task : Grasshopper - Personalized Message
```javascript
function greet (name, owner) {
  return name === owner ? 'Hello boss' : 'Hello guest';
}
```
#### CodeWars Task : Clean up after your dog
```javascript
function crap(x, bags, cap){
  const str = x.toString();
  if(str.includes('D')) return 'Dog!!'
  const crapCount = str.split('@').length - 1;
  return bags * cap >= crapCount ? 'Clean' : 'Cr@p';
}
```
#### CodeWars Task : Enumerable Magic #25 - Take the First N Elements
```javascript
function take(arr, n) {
  return arr.slice(0, n);
}
```
#### CodeWars Task : Will there be enough space?
```javascript
function enough(cap, on, wait) {
  return cap >= (on + wait) ? 0 : Math.abs(cap-on-wait);
}
```
#### CodeWars Task : For Twins: 1. Types
```javascript
function typeValidation(v, t) {
  return typeof(v) === t;
}
```
#### CodeWars Task : Beginner Series #1 School Paperwork
```javascript
function paperwork(n, m) {
  return n < 0 || m < 0 ? 0 : n * m;
}
```
#### CodeWars Task : Beginner Series #2 Clock
```javascript
function past(h, m, s){
  return  h * 3600000 + m * 60000 + s * 1000;
}
```
#### CodeWars Task : Filter out the geese
```javascript
function gooseFilter (birds) {
  const geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  return birds.filter(el => !geese.includes(el));
  
};
```
#### CodeWars Task : Reverse every other word in the string
```javascript
function reverse(str){
  if (str[0] === ' ') return '';
  let newStr = str.split(' ');
    for (let i = 0; i < newStr.length ; i++){
      if (i % 2) newStr[i] = newStr[i].split('').reverse().join('');
    }
  return newStr.join(' ');
}
```
#### CodeWars Task : Rock Paper Scissors!
```javascript
const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!';
  const getMsg = (n) => `Player ${n} won!`;

  if(p1 === 'scissors' && p2 === 'paper' ) return getMsg(1);
  if(p1 === 'paper' && p2 === 'scissors' ) return getMsg(2);
  
  if(p1 === 'paper' && p2 === 'rock' ) return getMsg(1);
  if(p1 === 'rock' && p2 === 'paper' ) return getMsg(2);
  
  if(p1 === 'rock' && p2 === 'scissors' ) return getMsg(1);
  if(p1 === 'scissors' && p2 === 'rock' ) return getMsg(2);
};
```
#### CodeWars Task : Is the string uppercase?
```javascript
String.prototype.isUpperCase = function() {
  return this.toUpperCase() == this;
}
```
#### CodeWars Task : Flatten and sort an array
```javascript
function flattenAndSort(array) {
  let myArray = [];
  array.forEach( el => {
    if(Number.isInteger(el)){
      myArray.push(el);
    } else if(Array.isArray(el) && el.length){
      myArray = [...myArray, ...el];
    }
  });
  return myArray.sort((a, b) => a-b);
}
```
#### CodeWars Task : The Office III - Broken Photocopier
```javascript
function broken(x){
  let res = '';
  for ( let i = 0; i < x.length; i++){
    res += x[i] === '0' ? '1' : '0';
  }
  return res;
}
```
#### CodeWars Task : I need more speed!
```javascript
function reverse(arr) { 
  let count = arr.length
   for (let i = 0; i < count / 2; i++){
    let el = arr[i]
    arr[i] = arr[count - 1 - i]
    arr[count - 1 - i] = el; 
   }
}
```
#### CodeWars Task : The 5 Love Languages
```javascript
function loveLanguage(partner,weeks) {
  let arr = [0 , 0 , 0 , 0 , 0];
  for (let i = 0, index = 0; i < weeks * 7 ; i++){
    index === 4 ? index = 0 : index++;
    if (partner.response(LOVE_LANGUAGES[index]) == "positive"){
       arr[index]++;
     } 
  }
  return LOVE_LANGUAGES[arr.indexOf(Math.max(...arr))];
}
```
#### CodeWars Task : The Office IV - Find a Meeting Room
```javascript
function meeting(x){
  return x.indexOf('O') < 0 ? 'None available!' : x.indexOf('O') ;
}
```
#### CodeWars Task : String average
```javascript
function averageString(str) {

  if (str.length == 0) return "n/a";
  
  let obj = {
    "zero":0,
    "one":1,
    "two":2,
    "three":3,
    "four":4,
    "five":5,
    "six":6,
    "seven":7,
    "eight":8,
    "nine":9
  };
  
  let newArr = [
    "zero",
    "one",
    "two",
    "three",
    "four",
    "five",
    "six",
    "seven",
    "eight",
    "nine"
  ];
  
  let arr = str.split(' ');
  let sum = 0;
  
  for(let i = 0; i < arr.length; i++){
    if(obj[arr[i]] !== undefined) {
      sum +=obj[arr[i]]
    } else {
      return "n/a"
    }
  }
  
  let avg = Math.floor(sum / arr.length);
  
  return newArr[avg];
  
}
```
#### CodeWars Task : Categorize New Member
```javascript
function openOrSenior(data){
  return data.map((el, i) => el[0] >= 55 && el[1] > 7 ? 'Senior' : 'Open');
}
```
#### CodeWars Task : Graceful Tipping
```javascript
function gracefulTipping(bill) {
  let billWithTips = Math.ceil(bill * 1.15);
  if(bill < 10){
    return billWithTips;
  } else {
   let zero = '0';
   let  divider = +('5' + zero.repeat(billWithTips.toString().length - 2 ));
   if (billWithTips % divider === 0 ){
     return billWithTips;
   } else {
     let num = Math.trunc(billWithTips / divider);
     return (num + 1) * divider;
   }
  }
};
```
#### CodeWars Task : The Office V - Find a Chair
```javascript
function meeting(x, need){
  if (!need) return 'Game On';
  let arr = [];
  let ch = need;
  for (let i = 0; i < x.length; i++){
  if(ch > 0){
    let c = x[i][1] - x[i][0].length;
    arr.push(c > 0 ? (c > ch ? ch : c) : 0);
    if (c > 0) ch -= c;
    } else {
      return arr
    }
  }
  return ch <= 0 ? arr : 'Not enough!';
}
```
#### CodeWars Task : Ordered Count of Characters
```javascript
var orderedCount = function (text) {
  return [...new Set(text)].map(letter => [letter, text.split(letter).length - 1]);
}
```
#### CodeWars Task : Naughty or Nice?
```javascript
function getNiceNames(people){
  let arr = []
  for(let i = 0; i < people.length; i++){
    if(people[i].wasNice){
      arr.push(people[i].name)
    }
  }
  return arr;
}

function getNaughtyNames(people){
  let arr = []
  for(let i = 0; i < people.length; i++){
    if(!people[i].wasNice){
      arr.push(people[i].name)
    }
  }
  return arr;
}
```
#### CodeWars Task : Row Weights
```javascript
function rowWeights(array){
  let sumTeam1 = 0;
  let sumTeam2 = 0;
  for (let i = 0; i < array.length; i++){
    if(i % 2 == 0){
      sumTeam1 +=array[i]
    } else {
      sumTeam2 +=array[i]
    }
  }
  
  return [sumTeam1, sumTeam2]
}
```
#### CodeWars Task : Find the middle element
```javascript
const gimme = function (arr) {
  let min = Math.min(...arr);
  let max = Math.max(...arr);
  for(let i = 0; i < arr.length;i++){
    if (arr[i] < max && arr[i] > min){
      return i;
    }
  }
};
```
#### CodeWars Task : Take a Ten Minute Walk
```javascript
function isValidWalk(walk) {
  if (walk.length != 10) return false;
  let ns = 0;
  let we = 0;
  for (let i = 0; i < 10;i++){
    if(walk[i] == 'n') ns++;
    if(walk[i] == 's') ns--;
    if(walk[i] == 'w') we++;
    if(walk[i] == 'e') we--;
  };
  return ns == 0 && we == 0;
};
```
#### CodeWars Task : Multiplication table
```javascript
multiplicationTable = function(size) {
  let arr = [];
  for(let i = 1; i <= size; i++){
    let newArr = [];
    for(let j = 1; j <= size; j++){
     newArr.push(i*j);
    }
    arr.push(newArr);
  }
  return arr;
}
```
#### CodeWars Task : Sorted? yes? no? how?
```javascript
function isSortedAndHow(array) {
  let asc = [...array].sort((a,b) => a-b).join('');
  let des = [...array].sort((a,b) => b-a).join('');
  return asc == array.join('') ? 'yes, ascending' : des == array.join('') ? 'yes, descending' : 'no';
};
```
#### CodeWars Task : Moving Zeros To The End
```javascript
const moveZeros = function (arr) {
  let newArr = [];
  let totalZeros = 0;
  for(let i = 0; i < arr.length; i++){
    if(arr[i] !== 0) newArr.push(arr[i])
    else totalZeros++;
  };
  for(let i = 0; i < totalZeros; i++){
    newArr.push(0);
  };
  return newArr;
};
```
#### CodeWars Task : Sum of odd numbers
```javascript
function rowSumOddNumbers(n) {
  let firstElement = n * n - (n - 1);
  let total = 0;
  let count = 0;
  while (count < n){
    if(firstElement % 2 !== 0){
      total += firstElement;
    } else {
      count++; 
    }
    firstElement++;
  };
  return total;
};
```
#### CodeWars Task : Find variable which breaks strict comparison!
```javascript
function findStrangeValue() {
  return NaN;
}
```
#### CodeWars Task : Get Planet Name By ID
```javascript
function getPlanetName(id){
  let obj = {
     1:'Mercury',
     2:'Venus',
     3:'Earth',
     4:'Mars',
     5:'Jupiter',
     6:'Saturn',
     7:'Uranus',
     8:'Neptune'
  }
  
  return obj[id];
}
```
#### CodeWars Task : Rock Paper Scissors Lizard Spock
```javascript
function rpsls(pl1,pl2){
  let rules = [
    "scissors paper",
    "paper rock",
    "rock lizard",
    "lizard spock",
    "spock scissors",
    "scissors lizard",
    "lizard paper",
    "paper spock",
    "spock rock",
    "rock scissors"
  ]
 
  if (rules.includes(pl1 + ' ' + pl2)) return 'Player 1 Won!';
  else if(pl1 == pl2) return 'Draw!';
  else return 'Player 2 Won!';
}
```
#### CodeWars Task : Find the Capitals
```javascript
function capital(capitals){
  let arr = [];
  for (let i = 0; i < capitals.length; i++){
    if (capitals[i].hasOwnProperty('state')) {
      arr.push(`The capital of ${capitals[i]['state']} is ${capitals[i]['capital']}`);
    }
    if (capitals[i].hasOwnProperty('country')){
     console.log(capitals.length)
      arr.push(`The capital of ${capitals[i]['country']} is ${capitals[i]['capital']}`);
    }
  }
  return arr;
}
```