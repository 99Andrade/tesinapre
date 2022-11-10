<template>
  <body>
  <div class="register">
    <div class="formulario">   
    <h1 class="title">Registrate</h1>
    <h3>Ingrese la Informacion que se solicite</h3>
    <form action class="form" @submit.prevent="register">
      <p>
        <label for="#email" class="colocar_email">Email<span class="obligatorio"></span></label>
                    <input type="text" name="introducir_email" id="email" required="obligatorio" placeholder="Escribe tu Correo Electronico">
      
    </p>
    <p>
        <label for="#password" class="form-label">Password<span class="obligatorio"></span></label>
                    <input
                      v-model="password" 
                      class="form-input"
                      type="password"
                       name="introducir_password"
                        id="password" 
                        required="obligatorio"
                         placeholder="Escribe tu contraseña">
      
    </p>
    <p>
        <label for="#password-repeat" class="form-label">Password<span class="obligatorio"></span></label>
                    <input 
                    v-model="passwordRepeat" 
                      class="form-input"
                    type="password" 
                    name="passwordRepeat" 
                    id="passwordrepeat"
                     required="obligatorio"
                     placeholder="Escribe tu contraseña Nuevamente">
      
    </p>
    <button type="submit" name="enviar_datos" id="enviar"><p>Iniciar Sección</p></button>
    <p class="aviso">
                  <span class="obligatorio"> * </span>los campos son obligatorios.
                </p>         
    </form>
  </div>
  </div>
</body>
</template>

<script>
export default {
  data: () => ({
    email: "",
    password: "",
    passwordRepeat: ""
  }),
  methods: {
    register() {
      console.log(this.email);
      console.log(this.password);
      console.log(this.passwordRepeat);
    }
  }
};
</script>
<style>
@import url(https://fonts.googleapis.com/css?family=Noto+Sans);


body{
  height: 100%; 
  font-family: 'Noto Sans', sans-serif;
  background-color:  #FFEBD2; 
}


.register{  
  width: 480px; 
  height:10 auto;
  margin: 0px auto;
  border-radius: 0px;  
  padding-top: 0px;
  padding-bottom: 0px;  
  background-color: #fbfbfb; 
  padding-left: 0px; 
}


input{
  background-color: #fbfbfb; 
  width: 408px; 
  height: 40px; 
  border-radius: 5px;  
  border-style: solid; 
  border-width: 1px; 
  border-color: #AF4F41; 
  margin-top: 10px;  
  padding-left: 10px;
  margin-bottom: 20px; 
}


textarea{
  background-color: #fbfbfb; 
  width: 300px; 
  height: 250px; 
  border-radius: 2px;  
  border-style: solid; 
  border-width: 1px; 
  border-color: #EB3E1B; 
  margin-top: 10px;  
  padding-left: 10px;
  margin-bottom: 20px; 
  padding-top: 15px; 
}


label{
  display:contents; 
  
  float: right;  
}


button{
  height: 45px; 
  padding-left: 5px;
  padding-right: 5px;   
  margin-bottom: 20px; 
  margin-top: 10px;   
  text-transform: uppercase;
  background-color:#EB3E1B; 
  border-color: #EB3E1B; 
  border-style: solid; 
  border-radius: 10px;  
  width: 420px;   
  cursor: pointer;
}


button p{
  color: #fff; 
}


span{
  color: #EB3E1B; 
}


.aviso{
  font-size: 13px;  
  color: #0e0e0e;  
}


h1{
  font-size: 39px;  
  text-align: letf; 
  padding-bottom: 20px; 
  color:#EB3E1B;
}


h3{
  font-size: 16px; 
  padding-bottom: 30px;
  color: #0e0e0e;   
}


p{
  font-size: 14px; 
  color: #0e0e0e; 
}


::-webkit-input-placeholder {
 color: #a8a8a8;
}


::-webkit-textarea-placeholder {
 color: #a8a8a8;
}


.formulario input:focus{
  outline:0;
  border: 1px solid #97d848;
}


.formulario textarea:focus{
  outline:0;
  border: 1px solid #97d848;
}
</style>