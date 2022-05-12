<template>
<div class="conatiner">
    <div class="login">
        <h1>Iniciar sesión</h1>
        <p>email: <input v-model="user.email" /></p>
        <p>password: <input v-model="user.password" /></p>
        <button class="btn" @click="ingresar">ingresar</button>
    </div>
</div>

</template>

<script>
import { getAuth, signInWithEmailAndPassword } from "firebase/auth";


export default {
  name: "LoginView",
  data() {
    return { user: { email: "", password: "" } };
  },
  methods: {
    async ingresar() {
      const { email, password } = this.user;
      const auth = getAuth();
      await signInWithEmailAndPassword(auth, email, password);
      console.log('next is now home')
      this.$router.push("/");
    },
  },
};
</script>

<style scoped>
.container{
  padding: 100vh;
}
.login{
  background: rgb(241, 108, 13);
  margin: 100px 500px;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
}

.btn{
  margin-top: 5px;
  padding: 8px 20px;
  border-radius: 10px;
  color: rgb(255, 255, 255);
  background-color: rgb(105, 3, 173);
}

h1, p{
  color: white;
}
p{
  text-align: right;
  margin: 0px 20px;
}
</style>
