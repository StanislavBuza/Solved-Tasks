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