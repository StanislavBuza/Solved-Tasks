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