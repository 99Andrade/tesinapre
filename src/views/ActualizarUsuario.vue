<template>
  <div  class="actualizarusuario">
    <h1 class="Actualizar Usuario">Actualizar Usuario</h1>
        <form action class="form" @submit.prevent="actualizarusuario">
          <label class="form-label" for="#nombreusuario">Nombre del Usuario:</label>
                <input
                v-model="nombreusuario"
                class="form-input"
                type ="nombreusuario"
                id="nombreusuario"
                required
                placeholder="Nombre del Usuario"
          >
          <label class="form-label" for="#usuario">Usuario:</label>
        <input
          v-model="usuario"
          class="form-input"
          type="usuario"
          id="usuario"
          placeholder="Usuario"
        >
        <label class="form-label" for="#password">Contraseña:</label>
        <input
          v-model="password"
          class="form-input"
          type="password"
          id="password"
          placeholder="Password"
        >
        <label class="form-label" for="#password-repeat">Repite la contraseña:</label>
      <input
        v-model="passwordRepeat"
        class="form-input"
        type="password"
        id="password-repeat"
        placeholder="Password"
      >
        <label class="form-label" for="#idrol">IdRol:</label>
        <input
          v-model="idrol"
          class="form-input"
          type="idrol"
          id="idrol"
          placeholder="IdRol"
        >
        <input class="form-submit" type="submit" value="Actualizar">
      </form>
     </div>
      </template>


<script>
export default {
  data: () => ({
    nombreusuario: "",
    usuario: "",
    password:"",
    idrol: ""
  }),
  methods: {
    actualizar() {
      console.log(this.nombreusuario);
      console.log(this.usuario);
      console.log(this.password);
      console.log(this.passwordRepeat);
      console.log(this.idrol);
    }
  }
};
</script>

<style lang="scss" scoped>
.register {
  padding: 2rem;
}
.title {
  text-align: center;
}
.form {
  margin: 3rem auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 20%;
  min-width: 350px;
  max-width: 100%;
  background: rgba(19, 35, 47, 0.9);
  border-radius: 5px;
  padding: 40px;
  box-shadow: 0 4px 10px 4px rgba(0, 0, 0, 0.3);
}
.form-label {
  margin-top: 2rem;
  color: white;
  margin-bottom: 0.5rem;
  &:first-of-type {
    margin-top: 0rem;
  }
}
.form-input {
  padding: 10px 15px;
  background: none;
  background-image: none;
  border: 1px solid white;
  color: white;
  &:focus {
    outline: 0;
    border-color: #1ab188;
  }
}
.form-submit {
  background: #1ab188;
  border: none;
  color: white;
  margin-top: 3rem;
  padding: 1rem 0;
  cursor: pointer;
  transition: background 0.2s;
  &:hover {
    background: #0b9185;
  }
}
.error {
  margin: 1rem 0 0;
  color: #ff4a96;
}
</style>


