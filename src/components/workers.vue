<template>
    <div class="card"></div>
    <div class="card"></div>
    <div class="card"></div>
  </template>

<script>
document.querySelectorAll(".card").forEach(card => {
  card.addEventListener("click", function() {
    console.log("click")
    this.classList.add("clicked");
  });
});

export default {
    name: "Worker-cards"
    
}
</script>

<style>
.card{
    width: 15vw;
    aspect-ratio: 3/4;
    background: linear-gradient(135deg, var(--secondary), var(--accent));
    transition: all 1s ease;
    border-radius: 13px;
}

.card:hover{
    scale: 1.2;
    box-shadow: 0px 0px 20px var(--primary);
    border-radius: 10px;
}

.card.clicked{
    transform: rotateX(180deg);
}
</style>