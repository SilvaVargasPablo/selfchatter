<template>
  <div class="registro">
    <h1 class="title">Crear nueva cuenta</h1>
    <p>email: <input v-model="user.email" /></p>
    <p>password: <input v-model="user.password" /></p>
    <button class="btn" @click="registrar">registrar</button>
  </div>
</template>

<script>
import { getAuth, createUserWithEmailAndPassword } from "firebase/auth";

export default {
  name: "RegistrarView",
  data() {
    return { user: { email: "", password: "" } };
  },
  methods: {
    async registrar() {
      const { email, password } = this.user;
      const auth = getAuth();
      await createUserWithEmailAndPassword(auth, email, password);
      this.$router.push("/chat");
    },
  },
};
</script>

<style scoped>
.registro{
  background: rgb(105, 3, 173);
  margin: 100px 500px;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
}

.btn{
  margin-top: 5px;
  padding: 8px 20px;
  border-radius: 10px;
  background-color: rgb(241, 108, 13);
  color: white;
}

h1, p{
  color: white;
}
p{
  text-align: right;
  margin: 0px 20px;
}
</style>
