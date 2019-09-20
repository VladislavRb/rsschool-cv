1. Vlad Rabashchenko  
2.  
    phone: +375 29 103 55 02  
    gmail: vlad.rabashchenko@gmail.com  
3. To be brief, my goal is to learn all the necessary front-end 
stuff like HTML, CSS and so on. When it comes to my wishes, I'd like 
myself 
not to be lazy so I can evolve:)  
4.  
  - HTML  
  - CSS  
  - JS (a bit)  
  - React (a bit too)  

5.
```javascript
function go(){
	let input = document.getElementsByTagName("input")[0].value;
	let arr = myMap(stringToArr(input), function(x){ return +x;});
	let textareas = [];
	for(let i = 0; i < 3; i++){
		let textarea = 
document.getElementsByTagName("textarea")[i];
		textarea.style.visibility = "visible";
		textareas.push(textarea);
	}
	textareas[1].style.width = "80px";
	textareas[2].style.width = "80px";
	if(myEvery(arr, function(x){return !Number.isNaN(x)})){
		textareas[0].value = bubbleSort(arr);
		textareas[1].value = "min : " + minInArray(arr) + ", max 
: " + maxInArray(arr);
		textareas[2].value = sum(arr);
	}
	else{
		textareas.forEach(x => x.value = "none");
	}
}
function push(arr, pos){
	for(let i = pos + 1; i < arr.length; i++){
		arr[i - 1] = arr[i];
	}
	arr.length--;
	return arr;
}
function stringToArr(string){
	let arr = [];
	let buffer = "";
	for(let sym of string){
		if(sym != " "){
			buffer += sym;
		}
		else{
			if(buffer != ""){
				arr.push(buffer);
			    buffer = "";
			}
		}
	}
	if(buffer != ""){
		arr.push(buffer);
	}
	return arr;
}
function bubbleSort(arr){
	for(let i = 0; i < arr.length; i++){
		for(let j = 0; j < arr.length - i; j++){
			if(arr[j] > arr[j + 1]){
				let temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
	return arr;
}
function minInArray(arr){
	let min = arr[0];
	for(let elem of arr){
		if(elem < min) min = elem;
	}
	return min;
}
function maxInArray(arr){
	let max = arr[0];
	for(let elem of arr){
		if(elem > max) max = elem;
	}
	return max;
}
function sum(arr){
	let result = 0;
	for(let number of arr){
		result += number;
	}
	return result;
}
function myMap(arr, func){
	for(let i = 0; i < arr.length; i++){
		arr[i] = func(arr[i]);
	}
	return arr;
}
function myEvery(arr, criteria){
	for(let elem of arr){
		if(!criteria(elem)){
			return false;
		}
	}
	return true;
}
```

6. -  
7. BSU, MMF, 2 course. Attended:  
  - one Python training  
  - one JS and several algorithms trainings  
  - Codecademy HTML and CSS.

8. Something near B2. Attended English Courses (SOL Minsk)
