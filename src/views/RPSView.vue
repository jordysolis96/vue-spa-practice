<script setup>
let choices = ["rock", "paper", "scissors"];
let choiceIndex = Math.floor((Math.random() * 3));
let player1 = choices[choiceIndex];
function playerChoice() {
  let choice = document.getElementById("choice");
  let text = choice.options[choice.selectedIndex].text;
  document.getElementById("userChoice").innerHTML = text;
}


</script>
<template>
  <h1 class="row justify-content-center">Lets play Rock, Paper, Scissors {{ player1 }}</h1>
  <form class="row g-3 justify-content-center">
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
  <h1 id="userChoice"></h1>
  <p id="timer"></p>
</template>
