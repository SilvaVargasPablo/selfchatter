<template>
  <div class="home">
    <img class="logo" alt="Vue logo" src="../assets/logo.png">
    <HelloWorld class="msg" msg="Vienvenido a SelfChatter"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style>

.home{
  margin-top: 20px;

}
img {
 max-width: 100%;
 max-height: 100%;
}
.logo {
 height: 90px;
 width: 100px;
}
.msg{
  color: white;
}

</style>
