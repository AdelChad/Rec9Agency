<template>
  <div class="greetings">
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Accueil</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Photographie</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Court métrage</a>
            </li>
          </ul>
        </div>
      </div>
    </nav> 
  </div>
</template>

<style scoped>

.menu{
  display: block;
  margin-left: auto;
  margin-right: auto;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
