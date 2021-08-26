<template>
  <div class="container">
      <header class="header">
          <h1 class="header-description">ali's task manager</h1>
          <ul class="links-wrapper">
              <li class="links"><nuxt-link to="/">Home</nuxt-link></li>
              <li class="links"><nuxt-link to="/Tasks">Tasks</nuxt-link></li>
          </ul>
      </header>
  </div>
</template>

<script>
export default {
name:'AppHeader',
}
</script>

<style scoped>
.header{
    display: flex;
    padding: 20px 0px;
    justify-content: space-around;
    background: rgb(214, 218, 219);
    align-items: center;
    border: 2px solid black;
}
.header-description{
    text-transform: uppercase;
    font-weight: 400;
}
.links-wrapper{
    display: flex;
    justify-content: space-between;
    flex-basis: calc(100%/7);
}
.links{
    list-style: none;
}
.links a{
    text-decoration: none;
    color: rgb(214, 218, 219);
    border: 1px solid transparent;
    background: black;
    padding: 5px;
    border-radius: 8px;
}
.links:hover{
    transform: scale(0.97);
}
</style>
