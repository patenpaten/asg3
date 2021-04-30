<!DOCTYPE html>
<html lang="en"><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">

<head>
	<title></title>
	<!-- preview, local storage,  -->

</head>
<link rel="stylesheet" href="colorpick.css">
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200&display=swap');
* {
  box-sizing: border-box;
}

body {

background:pink;
 /*radial-gradient(circle, rgba(174,238,222,1) 0%, rgba(216,233,148,0.7676348547717842) 100%);*/
  margin: 0;font-family: 'Poppins', sans-serif;
}

 }
/* Style the header */

.header {
	text-transform: uppercase;
  background-color: #f1f1f1;
  padding: 20px;
 
}

.header h1{
	font-size: 4em;
	text-align: center;
}

.header p{
	font-size: 18px;
	text-align: center;
}

/* Style the top navigation bar */
.topnav {

  position: sticky;
  top: 0;
  overflow: hidden;
  background-color: #333;

}

/* Style the topnav links */
.topnav a {
  letter-spacing: 3px;
  float: left;
  display:block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change color on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}

#content div{
	text-align: center;
	font-size: 2em;
}

/* Create three unequal columns that floats next to each other */
.column {
  float: left;
  padding: 10px;
}

/* Left and right column */
.column.side {
  width: 25%;

}

/* Middle column */
.column.middle {
  width: 50%;
  
}
img#white{
width: 80%;
height: 100%;
margin: left;
margin:right; 
z-index: -1;

}
two.jpg{
	z-index: 0;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {/*for tablets*/
  .column.side, .column.middle {
    width: 100%;
  
  }
#bgcolortemplate{
  	width: 25%;

}
}

@media screen and (max-width: 768px){/*for pc*/
#bgcolortemplate{
  	width: 100%;

}
}

#div1,#div2,#temp1{
  float: left;
  width: 125px;
  height: 85px;
  margin: 10px;
  padding: 10px;
  border: 1px solid black;

  
}
#div3,#div4,#temp2{
  float: left;
  width: 125px;
  height: 85px;
  margin: 10px;
  padding: 10px;


  
}

.resizer{
	text-align: center;
	font-size: 15px;
	
}

#bgcolortemplate{
  width: 100%;
  height: 700px;
 border-radius: 40px;
  background-color:white;
  border:10px solid transparent;
border-image: url('raw.jpg') 200 round;
width: 100%;

}

.flex-center{
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: column;
}

 


label{
	font-size: 600;
	margin-right: 35px;
	color:  #424242;
	font-size: 1.2em;

}
.row{
	display: flex;
	flex-wrap: wrap;
}
.footer{
	background-color: #24262b
	padding: 70px 0;
	}

.container{
	max-width: 2000px;
	background-color: black;
	margin: auto;
}
.footer-col{
	width: 25%;
	padding:0 15px;
	
}
.footer-col h3{
	font-size:18px;
	text-transform: capitalize;
	color: white;
	margin-bottom: 30px;
	font-weight: 500;
	position: relative;
}

ul{
	list-style: none;
}
.footer-col h3::before{
	content: '';
	position: absolute;
	left: 0;
	bottom:-10px;
	background-color: slateblue;
	box-sizing: border-box;
	height: 1px;
	width: 50px;
}

a:hover{
	color:yellow;
}
}
</style>
<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
 <script type="text/javascript">
    	var fs =2;
function textResizer(){

	var paragraph = document.querySelectorAll(".resizer"); 
	for (var i = 0; i < paragraph.length; i++) {
		fs=fs+1;
		paragraph[i].style.fontSize=fs+"em";
	}


}
function textDefault(){

	var paragraph = document.querySelectorAll(".resizer");
	for (var i = 0; i < paragraph.length; i++) {
		paragraph[i].style.fontSize="2em";
	}
}
    </script>
</head>
<body>

<div class="header">
  <h1>Customize your cooperate <br> invitation card!</h1>
  <p>Discover the platform that gives you the freedom to create and design your business template exactly as you want them!</p>
</div>

<div class="topnav">
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Services</a>
  <a href="#">Profile</a>
</div>

<div class="row">
  <div class="column side">
    <h2>Drag and drop the company!</h2>
    <p>Drag the company logo</p>
 	
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
  <img src="ikea.jpg" draggable="true" ondragstart="drag(event)" id="drag1" width="100" height="70">
</div>
<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)">
<img src="lego.png" draggable="true" ondragstart="drag(event)" id="drag2" width="100" height="70">
</div>
<div id="temp1" ondrop="drop(event)" ondragover="allowDrop(event)">
<img src="two.jpg" draggable="true" ondragstart="drag(event)" id="drag3" width="100" height="70">
</div>


<script type="text/javascript">
	function imgtransform(anything){
		document.querySelector('#bgcolortemplate').src=anything;
	}
</script>
</div>
<!-- dont delete the div kalau inda kacau -->
  
  
  <div class="column middle">
    <h2>Cooperative template</h2>
    <span id="edit">

<div id="div3" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<div id="div4" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<div id="temp2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

 	<div id="bgcolortemplate">
 		
 		<div class="resizer"><p contenteditable="true" style="font:Arial;" style="font-size:20px;"></p></div><br>
 		<br>
 		<label style="font-size: 15px;">Try changing the texts by clicking the text</label>
 		<div class="resizer"><p contenteditable="true" style="font:50px bold" style="font:Arial" style="text-align: center;">Annual <br> Member <br>Meeting</p></div>


 		<div class="resizer"><p contenteditable="true">December 15,2021 | 2pm-4pm <br>Rizkun Hotel</p></div><br>
 		<div class="resizer"><p contenteditable="true">Come annd join our annual business convention <br> Renowed guest speakers from well known companies will be there too!</p></div>
 		<div class="resizer"><p contenteditable="true" style="font:arial">RSVP</p></div>
 		<div class="resizer"><p contenteditable="true">+673 658 9032</p></div>

   </div>

    </span>
    
<div class="resizer">
	
<!-- <button onclick="textResizer()">Make font text bigger 2em</button>
<button onclick="textDefault()">Make font text default </button> -->


	</div>


  </div>
  

  <div class="column side">
    <h2>Drop some creative wordings into your template!</h2>
    <p>Be creative with color picker, change your font style and so on!</p>

    <div class="parent flex-center">
    <div class="input-container">
    	<label>Change the background color and click on the template</label>
    	<input type="Color" name="co" onchange="changeColor(this.value)">
    </div>	
    
    </div>
    <p>Relax your mind with listening to this song</p>
    <audio id="myAudio" controls>

  <source src="yt1s.com - Alif Satar Raihan  Sesungguhnya2019.mp3" type="audio/mpeg">

   </audio>

   
	
    <script type="text/javascript">
    	function changeColor(color){
    		document.getElementById('bgcolortemplate').style.backgroundColor = color
    	}
    </script><br>
    <body onload="get()">
    <p id="savedText"> </p>
    <p id="openedText"> </p>

    <input type="text" id="input"/>
    <button onclick="save()" style="background-color: slateblue">Preview card</button>

	</body>
    <script>

    	var storedItem=localStorage.getItem("storedItem");

    	function save(){
    		var Item = document.getElementById("input").value;
    		localStorage.setItem("storedItem",Item);
    		document.getElementById("savedText").innerHTML=Item+"SAVED"
    	}
    	function get(){
    		localStorage.getItem("storedItem");
    		document.getElementById("openedText").innerHTML=storedItem+"OPENED";
    	}
    </script>

  </div>
</div>	

<footer class="footer">
<div class="container">
	<div class="row">
		<div class="footer-col">
			<h3>Company</h3>
			<ul>
				<li><a href="#">About us</a></li>
				<li><a href="#">Our services</a></li>
				<li><a href="#">Privacy and policy</a></li>
				
			</ul>
		</div>
		<div class="footer-col">
			<h3>Help Service</h3>
			<ul>
				<li><a href="#">FAQ</a></li>
			</ul>
		</div>
		<div class="footer-col">
			<h3>Contact</h3>
			<ul>
				<li><a href="#">Head Company : +673 223 2222</a></li>
				<li><a href="#">Receptionist : +673 665 7878</a></li>
			</ul>
		</div>
		<div class="footer-col">
			<h3>Connect</h3>
			<div class="social-links">
				<a href="#"><i class="fab fa-facebook-f"></i></a>
				<a href="#"><i class="fab fa-twitter"></i></a>
				<a href="#"><i class="fab fa-instagram"></i></a>
				<a href="#"><i class="fab fa-youtube"></i></a>
			</div>
		</div>
	</div>
</div>
</footer>
</body>
</html>

