<template>
<div class="footer">
  <div class="footer-inner-div">
    <a href="tel:1-715-497-2268"><b-icon-phone></b-icon-phone>
    715-497-2268</a>
  </div>
  <div>
    <a href="mailto:connormcraven@gmail.com"><b-icon-envelope></b-icon-envelope>
    connormcraven@gmail.com</a>
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
    flex-wrap: wrap;
    justify-content: space-evenly;
    align-items: center;
    color: white;
    background-color: darkslategray;
    font-size: 1em !important;
    padding: .5rem 0;
  }

  a:link {
    text-decoration: none;
  }

  .footer-inner-div {
    margin-right: 2rem;
  }
</style>
