# IGCSE-Edexcel-Biology---1.1-Characteristics-of-living-organisms<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Cell Flashcards</title>

<style>
body{
font-family:Arial,sans-serif;
text-align:center;
padding:20px;
}

.card{
width:500px;
margin:auto;
padding:30px;
border:2px solid #4CAF50;
border-radius:15px;
font-size:24px;
min-height:150px;
display:flex;
align-items:center;
justify-content:center;
cursor:pointer;
}

button{
margin:10px;
padding:10px 20px;
font-size:16px;
}
</style>
</head>

<body>

<h2>eScience Flashcards</h2>

<div class="card" onclick="flipCard()" id="card">
What is the function of the nucleus?
</div>

<br>

<button onclick="previousCard()">Previous</button>
<button onclick="nextCard()">Next</button>

<p id="progress"></p>

<script>

const cards = [

{
q:"What is the function of the nucleus?",
a:"Controls all activities of the cell."
},

{
q:"What is the function of the cell membrane?",
a:"Controls movement of substances in and out."
},

{
q:"What is the function of mitochondria?",
a:"Site of aerobic respiration."
}

];

let current=0;
let showingAnswer=false;

function displayCard(){
document.getElementById("card").innerHTML=
showingAnswer ? cards[current].a : cards[current].q;

document.getElementById("progress").innerHTML=
(current+1)+" / "+cards.length;
}

function flipCard(){
showingAnswer=!showingAnswer;
displayCard();
}

function nextCard(){
current=(current+1)%cards.length;
showingAnswer=false;
displayCard();
}

function previousCard(){
current=(current-1+cards.length)%cards.length;
showingAnswer=false;
displayCard();
}

displayCard();

</script>

</body>
</html>
