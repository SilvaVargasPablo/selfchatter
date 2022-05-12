<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Este es un chat donde pordras escribir y responderte a ti mismo por que no teines amigos y estas super solo ekisde.
    </p>
    <div class="logo">
      <img  src="../assets/chat.png" alt="">
    </div>
    
  </div>
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
img {
  margin-top: 30px;
  max-width: 100%;
  max-height: 100%;
}

.logo {
 height: 600px;
 width: 100%;
}
p{
  color: white;
  font-size: 1.2rem;
  font-weight: 400;
}

</style>
