<template>
  <ul>
    <a href="#"><img src="../assets/logo-new.png"/></a>
    <li>
      <a href="#home"><img src="../assets/search.png"/></a>
    </li>
    <li><a href="#news">Register</a></li>
    <li><a href="#contact">Discover</a></li>
    <li><a class="active" href="#about">Home</a></li>
  </ul>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped lang="scss">
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: rgb(250, 250, 250);
  a {
    float: left;
    width: 10em;
    img {
      max-width: 60px;
    }
    &:hover:not(.active) {
      width: 11em;
    }
  }
}

li {
  float: right;
  width: 10em;
  padding: 0.5em 0 0.5em 0;
  a {
    display: block;
    color: rgb(56, 56, 56);
    text-align: center;
    padding: 8px 10px;
    text-decoration: none;
    img {
      max-height: 20px;
    }
    &:hover:not(.active) {
      background-color: rgb(231, 230, 230);
      border-radius: 30px;
      width: 8em;
    }
  }
  .active {
    background-color: #d4d4d4;
    border-radius: 30px;
  }
}
</style>
