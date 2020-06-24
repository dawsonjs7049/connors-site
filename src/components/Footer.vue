<template>
<div class="footer">
  <div>
    <b-icon-phone></b-icon-phone>
    715-666-6666
  </div>
  <div>
    <b-icon-envelope></b-icon-envelope>
    connor@gmail.com
  </div>

</div>
  <!-- <h1>{{ msg }}</h1> -->
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .footer {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-evenly;
    align-items: center;
    height: 3rem;
    color: white;
    background-color: darkslategray;
    font-size: 1.5em;
  }
</style>
