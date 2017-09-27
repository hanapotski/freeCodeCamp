# JSON, APIs and Ajax

### APIs
* Application Programming Interfaces - are tools that computers use to communicate with one another.
* Most web APIs transfer data in a format called JSON. JSON stands for JavaScript Object Notation.
* JSON is nothing more than object properties and their current values, sandwiched between a { and a }.
* These properties and their values are often referred to as "key-value pairs".

#### Get JSON with the jQuery getJSON Method
$.getJSON("/json/cats.json", function(json) {
        $(".message").html(JSON.stringify(json));
      });

#### Convert JSON Data to HTML
json.forEach(function(val) {
  var keys = Object.keys(val);
  html += "<div class = 'cat'>";
  keys.forEach(function(key) {
    html += "<strong>" + key + "</strong>: " + val[key] + "<br>";
  });
  html += "</div><br>";
});


#### Render Images from Data Sources
html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";


#### Prefilter JSON
json = json.filter(function(val) {
  return (val.id !== 1);
});


#### Get Geolocation Data
if (navigator.geolocation) {
  navigator.geolocation.getCurrentPosition(function(position) {
    $("#data").html("latitude: " + position.coords.latitude + "<br>longitude: " + position.coords.longitude);
  });
}
