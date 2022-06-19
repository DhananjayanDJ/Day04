1.Use the same rest countries and print all countries name, region, sub region and population

var request= new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function(){
var result=JSON.parse(request.response);
for(i=0;i<result.length;i++)
{
   console.log("The name is " + result[i].name+" The region is  "+result[i].region+" The sub-region is   "+result[i].subregion+" The population is  "+result[i].population);
}

}

2.Use the rest countries API url -> https://restcountries.eu/rest/v2/all and display all the country flags in console.


var request= new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function(){
var result=JSON.parse(request.response);
for(i=0;i<result.length;i++)
{
   console.log("the Name of the country is " + result[i].name+" The country flag is "+result[i].flag);
}

}


3How to compare two JSON have the same properties without order?
var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };

var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };
console.log(JSON.stringify(obj1)===JSON.stringify(obj2));

