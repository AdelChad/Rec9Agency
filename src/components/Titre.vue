<template>
    <div>
        <section class="menu">
            <div class="top">rec9 agency</div>
            <div class="bottom" aria-hidden="true">rec9 agency</div>
        </section>
    </div>
</template>

<style>
.menu {
    display: grid;
    place-content: center;
    background-color: #333;
    height: 10vh;
    font-family: policeTitre;
    font-size: 5vh;
    font-weight: 700;
    text-transform: uppercase;
    color: var(--text-color);
  }
  
  .menu > div {
    grid-area: 1/1/-1/-1;
  }
  .top {
    clip-path: polygon(0% 0%, 100% 0%, 100% 48%, 0% 58%);
  }
  .bottom {
    clip-path: polygon(0% 60%, 100% 50%, 100% 100%, 0% 100%);
    color: rgb(218, 218, 218);
    background: -webkit-linear-gradient(177deg, black 53%, var(--text-color) 65%);
    background: linear-gradient(177deg, black 53%, var(--text-color) 65%);
    background-clip: text;
    -webkit-background-clip: text;
    transform: translateX(-0.02em);
  }
</style>