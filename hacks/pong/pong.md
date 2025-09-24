---
layout: opencs
title: Pong Game
permalink: /pong/
---

Controls:
W/S to move and D to shoot (Left Player)
Arrow Up/Down to move and Arrow Left to shoot (Right Player)
Bullets freeze enemy paddles for 5 seconds

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.sidebar {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}
.sidebar a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}
.sidebar a:hover {
  color: #f1f1f1;
}
.sidebar .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}
.openbtn {
  font-size: 20px;
  cursor: pointer;
  background-color: #111;
  color: white;
  padding: 10px 15px;
  border: none;
}
.openbtn:hover {
  background-color: #444;
}
#main {
  transition: margin-left .5s;
  padding: 16px;
}
/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidebar {padding-top: 15px;}
  .sidebar a {font-size: 18px;}
}
</style>
</head>
<body>

<div id="LessonSidebar" class="sidebar">
	<div>
	<br/>
	<h2><b>CS Concept Lesson</b></h2>
	<br/>
	<h3> Easy Concept: Mathematical Expressions </h3>
	<br/>
	</div>
	<br/>

  	<button type="button" onclick="closeNav()" style="padding: 15px 30px; cursor:pointer;">
	Close Lesson
	</button>
</div>

<div id="main">
  <button class="openbtn" onclick="triggerNav()">☰ Open Lesson</button>  
</div>

<script>
var sidebarOpen = false;

function triggerNav() {
	if (!sidebarOpen)
	{
		document.getElementById("LessonSidebar").style.width = "400px";
  		document.getElementById("main").style.marginLeft = "250px";
		sidebarOpen = true;
	}
	else
	{
		document.getElementById("LessonSidebar").style.width = "0";
  		document.getElementById("main").style.marginLeft= "0";
		sidebarOpen = false;
	}
}

function closeNav() {
  document.getElementById("LessonSidebar").style.width = "0";
  document.getElementById("main").style.marginLeft= "0";
}
</script>


<script src="{{site.baseurl}}/hacks/pong/pong.js"></script>
   
</body>
</html> 