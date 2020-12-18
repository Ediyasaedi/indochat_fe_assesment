<template>
  <div>
    <div class="container">
      <img src="../assets/getintouch.png" alt="" />
      <h3>Get in Touch</h3>
      <span
        >Want to get in touch? We'd love to hear from you. Here's how you can
        reach us.</span
      >

      <div class="row">
        <div class="col-50">
          <h2>This is Map</h2>
        </div>

        <div class="col-50">
          <h2>Feedback</h2>
          <div>
            <form>
              <div class="row">
                <div class="col-50">
                  <input
                    type="text"
                    id="fname"
                    name="first"
                    placeholder="First"
                  />
                </div>
                <div class="col-50">
                  <input
                    type="text"
                    id="lname"
                    name="last"
                    placeholder="Last"
                  />
                </div>
              </div>
              <input
                type="text"
                id="email"
                name="email"
                placeholder="your@mail.com"
              />
              <input
                type="textarea"
                id="message"
                name="message"
                placeholder="Message"
              />
              <input type="submit" value="Send" class="btn" />
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GetInTouch",
};
</script>

<style scoped lang="scss">
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 40px;
  margin-bottom: 40px;
}

.row {
  display: -ms-flexbox; /* IE10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE10 */
  flex-wrap: wrap;
}

.col {
  padding: 0 16px;
  &-25 {
    -ms-flex: 25%; /* IE10 */
    flex: 25%;
  }
  &-50 {
    -ms-flex: 50%; /* IE10 */
    flex: 50%;
  }
  &-75 {
    -ms-flex: 75%; /* IE10 */
    flex: 75%;
  }
}

.container {
  background-color: #f2f2f2;
  padding: 5px 20px 15px 20px;
  border: 1px solid lightgrey;
  border-radius: 3px;
}

input {
  &[type="text"] {
    width: 100%;
    margin-bottom: 10px;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  &[type="textarea"] {
    width: 100%;
    height: 10em;
    margin-bottom: 20px;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
}

.icon-container {
  margin-bottom: 20px;
  padding: 7px 0;
  font-size: 24px;
}

.btn {
  float: left;
  background-color: #6493c9;
  color: white;
  padding: 12px;
  border: none;
  width: 50%;
  border-radius: 3px;
  cursor: pointer;
  font-size: 17px;
  &:hover {
    background-color: #3b75cc;
  }
}

a {
  color: #2196f3;
}

hr {
  border: 1px solid lightgrey;
}

/* Responsive layout - when the screen is less than 800px wide, make the two columns stack on top of each other instead of next to each other (also change the direction - make the "cart" column go on top) */
@media (max-width: 600px) {
  .row {
    flex-direction: column-reverse;
  }
  .col-25 {
    margin-bottom: 20px;
  }
}
</style>
