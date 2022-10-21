<script setup>
let choices = ["Rock", "Paper", "Scissors"];
let choiceIndex = Math.floor((Math.random() * 3));
let player1 = choices[choiceIndex];
function playerChoice() {
  let choice = document.getElementById("choice");
  let text = choice.options[choice.selectedIndex].text;
  if(text === "select rock, paper, or scissor"){
    document.getElementById("error").innerHTML = "Please choose rock, paper, or scissor in order to play"
    document.getElementById("timer").innerHTML = "You have to choose an item first -.-";
    document.getElementById('userChoice').innerHTML = "<img src=\"https://pbs.twimg.com/media/EbAU0n_WsAIQ0bg.jpg\" width=\"400px\" height=\"400px\" class=\"row col-5 justify-content-center\">";
    return
  }
  updateTimer();
  var intervalId = setInterval(updateTimer, interval)
}
var timer = 4;
var interval = 1500;
// TODO: This function needs to be called once every second
function updateTimer() {
  if(timer == 0){
    let choice = document.getElementById("choice");
    let text = choice.options[choice.selectedIndex].text;
    if((text === "Rock" && player1 === "Rock") || (text === "Scissors" && player1 === "Scissors") || (text === "Paper" && player1 === "Paper")){
      document.getElementById("timer").innerHTML = "It's a tie!";
      document.getElementById('userChoice').innerHTML = "<img src=\"https://i.skyrock.net/4238/87434238/pics/3239977525_1_3_r4KZex6F.jpg\" width=\"400px\" height=\"400px\" class=\"row col-4 justify-content-center\">";
    }else if((text === "Rock" && player1 === "Scissors") || (text === "Scissors" && player1 === "Paper") || (text === "Paper" && player1 === "Rock")){
      document.getElementById("timer").innerHTML = "You win!"
      document.getElementById('userChoice').innerHTML = "<img src=\"https://i.quotev.com/iujuli6rxsfa.jpg\" width=\"400px\" height=\"400px\" class=\"row col-4 justify-content-center\">";
    }else if((text === "Rock" && player1 === "Paper") || (text === "Scissors" && player1 === "Rock") || (text === "Paper" && player1 === "Scissors")) {
      document.getElementById("timer").innerHTML = "You lose!"
      document.getElementById('userChoice').innerHTML = "<img src=\"https://i.pinimg.com/564x/cc/76/72/cc7672071ebc0ea44c8fbc3accb6da5e.jpg\" width=\"400px\" height=\"400px\" class=\"row col-4 justify-content-center\">";
    }
    document.getElementById("restart-btn").innerHTML = "<button type=\"button\" class=\"btn btn-dark\" id=\"submit-btn\">Play again?</button>"
  }else if (timer == 1) {
    // document.getElementById('timer').innerHTML = "<img src=\"https://www.mypokecard.com/my/galery/agGsgHRnCz7Y.jpg\" width=\"100px\" height=\"150px\" class=\"row col-1 justify-content-center\">";
    document.getElementById('timer').innerHTML = "SHOOT!";
    document.getElementById('userChoice').innerHTML = "<img src=\"https://www.mypokecard.com/my/galery/agGsgHRnCz7Y.jpg\" width=\"400px\" height=\"400px\" class=\"row col-3 justify-content-center\">";
  } else if (timer == 2) {
    document.getElementById('timer').innerHTML = "Scissors";
    document.getElementById('userChoice').innerHTML = "<img src=\"https://product-images.tcgplayer.com/219373.jpg\" width=\"400px\" height=\"400px\" class=\"row col-3 justify-content-center\">";
  }else if (timer == 3) {
    document.getElementById('timer').innerHTML = "Paper";
    document.getElementById('userChoice').innerHTML = "<img src=\"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSW2q0bstP5Aawuyc-XEGkvTzERbL9KxA6TjQ&usqp=CAU\" width=\"400px\" height=\"400px\" class=\"row col-3 justify-content-center\">";
  }else if (timer == 4) {
    document.getElementById("error").innerHTML = "";
    document.getElementById('timer').innerHTML = "ROCK";
    document.getElementById('userChoice').innerHTML = "<img src=\"https://www.wired.com/images_blogs/gamelife/2010/03/rockmario.jpg\" width=\"400px\" height=\"400px\" class=\"row col-3 justify-content-center\">";
  }

  timer--;
}

function restart() {
  location.reload();
}
</script>
<template>
  <h1 class="row justify-content-center">Lets play Rock, Paper, Scissors :)</h1>
  <br>
  <form class="row g-3 justify-content-center">
    <span id="error" class="row col-12 justify-content-center" style="color: red"></span>
    <div class="col-4">
      <select class="form-select form-select-sm" aria-label=".form-select-sm example" id="choice">
        <option selected class="text center">select rock, paper, or scissor</option>
        <option value="1">Rock</option>
        <option value="2">Paper</option>
        <option value="3">Scissors</option>
      </select>
    </div>
    <div class="col-4">
      <button type="button" class="btn btn-dark w-100" id="submit-btn" v-on:click="playerChoice">Let's play!</button>
    </div>
  </form>
  <br>
  <h1 id="timer" class="row col-12 justify-content-center"></h1>
  <br>
  <h1 id="userChoice" class="row col-12 justify-content-center"></h1>
  <div class="row justify-content-center"><span id="restart-btn" class="row col-5 justify-content-center" v-on:click="restart"></span></div>
</template>
