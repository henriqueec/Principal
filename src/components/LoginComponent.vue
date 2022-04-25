<template>
  <v-container fluid>
      <v-row>
          <!--coluna 1 -->
          <v-col cols="6" align="center" style="padding: 0px 164px">
              <v-img 
              src="../assets/Logowilly.png"
              class="logowilly"
              ></v-img>
                <h3 class="text-center pt-10 mt-7 mb-7 white--text"> Um novo jeito de realizar vistorias. Fácil, rápido e prático. </h3>
                <v-text-field 
                    dark
                    solo
                    label="E-mail"
                    aria-required=""
                ></v-text-field>
                <v-text-field
                    dark
                    solo                                                                                                    
                    label="Senha"
                    type="password"
                    required
                ></v-text-field>
                <!-- Coluna dentro da coluna -->
                <v-row>
                    <v-col class="col-md-6 text-left">
                        <a href="#" class=" white--text"> Esqueci a senha</a>
                    </v-col>
                    <v-col class="col-md-6 text-right">
                        <v-btn class="btn white--text">Entrar </v-btn>
                    </v-col>
                    <v-col class="col-md-6 text-left">
                        <a href="#" class="white--text">Ainda não tem conta?</a>
                    </v-col>
                    <v-col class="col-md-6 text-right">
                        <a href="#" class="white--text orange--text">Conheça a Willfly?</a>
                    </v-col>
                </v-row> 
                <hr class="mt-8 mb-5">;
                <v-row>
                    <v-col class="col-md-2">
                        <v-img src="../assets/w.png" class="logow"></v-img>
                    </v-col> 
                
                    <v-col class="col-md-10">
                        <p class="d-flex white--text"> <strong>Quer ser um willy? </strong> <a href="#" class="orange--text">Clique e saiba como </a></p>
                    </v-col>
                </v-row>   
          </v-col>
          <!--coluna 2 -->
          <v-col cols="6">
              <img src="../assets/logohomem.png" class="imghomem">
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style scoped>
.logowilly {
    max-width: 30%;
    margin-top: 10%;
    background-size: auto;
}

.btn {
    padding: 15px 46px !important;
    background: linear-gradient(
    270deg,
    #ed8b20,
    #e96c29,
    #e55031,
    #e23b37,
    #e12c3b,
    #df243d,
    #df213e
  );
}

.logow {
    width: 100px;
}
.imghomem{
    background-size: 100px 300px;
    background-repeat: no-repeat;
    background-position: center;
}

hr{
 border-color: #e4730a; 
}

a {
  text-decoration: none;
}
</style>