
# Udacity APJ/Into to AJAX Project

### Purpose: To begin getting familiar with using API calls

#### What Does This Page Do

> This project asks the user to input an address into the form container
> Using the user's input address we make an AJAX call to the Google Maps
> API to get an image of the address that becomes the background of the
> page, we make a call to the NYT Article API which gets articles based
> on the city, and we make a call to the Wikipedia API to get topics
> about the city.

> With the NYT and Wikipedia calls I have coded an error function in
> case the user's input is incorrect or there isn't any information about
> the city requested.

#### How to Run Code

1. Drag the index.html file to your browser window
2. Type in the Street Address and City of where you want to live

#### Baisc Code Breakdown

```JQuery for Google Maps API to make background for website
$body.append( Google Image web address);

```JSON for NYT
 $.getJSON(NYTUrl, function(data) {
 	 //makes API and returns information

 }). error(function(e) {
 	//if API call fails, display this text
 })

 ```AJAX for Wikipedia
 $.ajax({
 	url: TEXT here,
 	datatype: "jsonp",
 	success: function(response) {
 		// makes API call and returns articles
 		clearTimeOut() // if the response isn't successful it calls this function
 	}
 })
