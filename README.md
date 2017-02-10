<!DOCTYPE html>
<!--
Created using JS Bin
http://jsbin.com

Copyright (c) 2017 by krisztafa (http://jsbin.com/huqumil/14/edit)

Released under the MIT license: http://jsbin.mit-license.org
-->
<meta name="robots" content="noindex">
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <link href="https://fonts.googleapis.com/css?family=Pangolin" rel="stylesheet">
  <title>Szín-óra</title>
<style id="jsbin-css">
*{
  margin: 0;
  padding: 0;
}

html, body{
  height: 100%;
}

#clock{
  text-align: center;
  position: relative;
  top: 50%;
  font-family: 'Pangolin', cursive;
  font-size: 150px;
  margin: -75px;
}


</style>
</head>
<body>
  <div id="clock">12:13:14</div>
<script id="jsbin-javascript">
function colorClock(){
var date= new Date();
var hours= date.getHours();
var minutes= date.getMinutes();
var seconds= date.getSeconds();

if(hours < 10){
  hours= '0' + hours;
}
if(minutes < 10){
  minutes= '0' + minutes;
}
if(seconds < 10){
  seconds= '0' + seconds;
}


var clockFace= hours+'¤'+minutes+'¤'+seconds;
var hexColor='#' + (10 + minutes) + (hours - 1) + seconds;


document.getElementById('clock').innerHTML= clockFace;
document.body.style.background= hexColor;

setTimeout(function(){
   colorClock();
  }, 1000);
}

colorClock();

</script>
</body>
</html>
