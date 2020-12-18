<template>
  <div>
    <div class="thumbnail text-center">
      <img src="../assets/banner.png" alt="" />
      <div class="caption">
        <span>
          <strong>Booked Tool</strong> enables you to <br />create Interactive
          Advertisement
        </span>
        <br />
        <button class="button">What is it?</button>
      </div>
    </div>

    <div class="container">
      <form class="form-inline">
        <label
          >Please login to start using <br /><strong>Booked Tool</strong></label
        >
        <input type="email" id="email" placeholder="Email" name="email" />
        <input type="password" id="pwd" placeholder="Password" name="pswd" />
        <button type="submit">Login</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped lang="scss">
.thumbnail {
  position: relative;
  margin-bottom: 0;
  border: 0;
  border-color: transparent;
}

.caption {
  position: absolute;
  top: 40%;
  left: 0;
  width: 75%;
  span {
    font-size: 1.5em;
  }
  .button {
    background-color: #6aa7d8;
    border: none;
    border-radius: 0.5em;
    color: whitesmoke;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    cursor: pointer;
  }
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 150px;
  background-color: rgb(212, 209, 209);
}

.form-inline {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  label {
    margin: 5px 10px 5px 0;
    text-align: left;
  }
  input {
    vertical-align: middle;
    margin: 5px 10px 5px 0;
    padding: 10px;
    background-color: #fff;
    border: 1px solid #ddd;
  }
  button {
    padding: 10px 20px;
    background-color: dodgerblue;
    border: 1px solid #ddd;
    border-radius: 0.5em;
    color: white;
    cursor: pointer;
    &:hover {
      background-color: royalblue;
    }
  }
}

@media (max-width: 800px) {
  .form-inline input {
    margin: 10px 0;
  }

  .form-inline {
    flex-direction: column;
    align-items: stretch;
  }
}

@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
</style>
