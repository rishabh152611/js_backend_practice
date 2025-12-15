# Projects related to DOM

## project link
[Click here](
https://stackblitz.com/edit/dom-project-chaiaurcode-be3zgfcp?file=2-BMICalculator%2Fchaiaurcode.js
)

#Solution code
##Project 1
const buttons =document.querySelectorAll(".button")
const body = document.querySelector("body");
buttons.forEach(function(button){

button.addEventListener("click", function(e){

  if(e.target.id==="grey"){
    body.style.backgroundColor=e.target.id; 
  }
  else if(e.target.id==="white"){
    body.style.backgroundColor=e.target.id; 
  }
  else if(e.target.id==="blue"){
    body.style.backgroundColor=e.target.id; 
  }
  else if(e.target.id==="yellow"){
    body.style.backgroundColor=e.target.id; 
  }
})

})
```
## project 2 solution
 const form = document.querySelector('form');
 form.addEventListener('submit',function(e){
   e.preventDefault();
   const height= parseInt(document.querySelector('#height').value);
   const weight= parseInt(document.querySelector('#weight').value);
   const results = document.querySelector("#results");
   if(height===""||height<0||isNaN(height)){
     results.innerHTML=`Please give a valid height ${height}`;
   }
   if(weight===""||weight<0||isNaN(weight)){
    results.innerHTML=`Please give a valid height ${weight}`;
  }
  else{
    const bmi = (weight/((height*height)/10000)).toFixed(2);
    if(bmi<19){
      results.innerHTML=`<snan>your bmi is ${bmi} and you are underweight</snap>`
    }
    if(bmi>=19&&bmi<=25){
      results.innerHTML=`<snan>your bmi is ${bmi} and your weight is perfect</snap>`
    }
    else if(bmi>25){
      results.innerHTML=`<snan>your bmi is ${bmi} and you are overweight</snap>`
    }
   
  }
 })
###project3 clock:
const clock = document.getElementById('clock');

setInterval(function(){
let date = new Date();

clock.innerHTML=date.toLocaleTimeString();
//console.log(date)
},1000);


