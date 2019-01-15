# JavaScript Object/Scope Classwork

1. What is the result of the following code? Explain your answer.
  
//console.log(obj.prop.getFullname());

--prints Aurelio De Rose: because it is within the scope of obj/prop/getFullname()
in which the getFullname function is to return 'this.fullname'; which within prop is Aurelio De Rose

//console.log(test());
--prints out John Doe because it is printing from the Global Scope, which applies to 'var fullname'



  var fullname = 'John Doe';
  var obj = {
     fullname: 'Colin Ihrig',
     prop: {
        fullname: 'Aurelio De Rosa',
        getFullname: function() {
           return this.fullname;
        }
     }
  };

  
  console.log(obj.prop.getFullname());


  var test = obj.prop.getFullname;

  
  console.log(test());




2. What will you see in the console for the following example?

//b() will return 10; who's function returns a, which equals 10

//console.log(a) will return 1; because it is outside of the 'b' function, therefore applies to 'var a'


  
  var a = 1; 
  function b() { 
      a = 10; 
      return; 
      function a() {} 
  } 
  b(); 
  console.log(a);    
  ```

* Create an array called ```peopleList``` objects using *Object Literal* notation. 

* Each 'person' object in the 'people' collection should have the following information:

First Name
Last Name
Age
Zip Code

Add the following 4 People to your list:
```
Jimmy Page, 62, 00821

Rick Nielsen, 57, 61016

Jimi Hendrix, 58, 90001

Lemmy Kilmister, 57, 21120




var peopleList =

    [firstname, lastname, age, zipcode];

    includedIn =
        [ {firstname: "Jimi", lastname: "Page", age: 62, zipcode: 00821},
        {firstname: "Rick", lastname:"Nielson", age: 57, zipcode: 61016},
        {firstname:"Jimi", lastname:"Hendrix", age: 58, zipcode: 90001},
        {firstname:"Lemmy", lastname:"Kilmister", age: 57, zipcode:21120};]





### Add code to perform the following:

* Dynamically add the property ```famousSong``` to the object instance for ```Jimi Hendrix``` and assign it the value ```Purple Haze```

* Dynamically add a function called ```getBandandZip()``` to the object instance for ```Jimmy Page``` that returns a concatenated string of ```Led Zeppelin HISZIPCODE``` (get zip code from the object instance). Call the function from your code and log the response.

* Write a function that accepts a zip code parameter and prints out all the people in the array with a matching zip code, or print the message ```No match found for zip code!``` if there is no match


