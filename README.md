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
