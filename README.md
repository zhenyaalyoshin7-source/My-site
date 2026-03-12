<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Calculator</title>

<style>

body{
font-family: Arial, sans-serif;
background: linear-gradient(135deg,#ff4e8a,#6a5cff);
height:100vh;
display:flex;
align-items:center;
justify-content:center;
margin:0;
color:white;
}

.container{
background: rgba(0,0,0,0.35);
backdrop-filter: blur(10px);
padding:40px;
border-radius:20px;
width:320px;
text-align:center;
box-shadow:0 10px 40px rgba(0,0,0,0.4);
}

h1{
margin-bottom:20px;
}

input{
width:100%;
padding:12px;
margin:8px 0;
border:none;
border-radius:10px;
font-size:16px;
}

button{
margin-top:10px;
padding:12px;
width:100%;
border:none;
border-radius:10px;
background:#ff4e8a;
color:white;
font-size:16px;
cursor:pointer;
transition:0.3s;
}

button:hover{
background:#ff2e73;
}

.result{
margin-top:20px;
font-size:20px;
font-weight:bold;
}

</style>
</head>

<body>

<div class="container">

<h1>❤️ Love Calculator</h1>

<input id="name1" placeholder="Your name">
<input id="name2" placeholder="Partner name">

<button onclick="calculate()">Calculate Love</button>

<div class="result" id="result"></div>

</div>

<script>

function calculate(){

let name1=document.getElementById("name1").value;
let name2=document.getElementById("name2").value;

if(name1=="" || name2==""){
alert("Enter both names");
return;
}

let loveScore=Math.floor(Math.random()*100)+1;

let message="";

if(loveScore>70){
message="Great match ❤️";
}
else if(loveScore>30){
message="Not bad 🙂";
}
else{
message="Maybe just friends 🤝";
}

document.getElementById("result").innerHTML=
name1+" ❤️ "+name2+"<br>"+loveScore+"%<br>"+message;

}

</script>

</body>
</html>
