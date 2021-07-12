<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <h1>Edrafox</h1>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://edrafox.com/index.html"
        target="_blank"
        text
      >
        <span class="mr-2">Saiba sobre nós</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <v-col >
            <v-container>
              <div>
                <carousel></carousel>
              </div>
            </v-container>
          </v-col>
          <v-col>  
            <principal>     
            </principal>
          </v-col>  
        </v-row>   
      </v-container>
      <div class="container">
        <div class="card">
          <div class="imgBx">
            <img src="https://repositorio.ufsc.br/bitstream/handle/123456789/105942/Free.jpg?sequence=1&isAllowed=y">
          </div>
          <div class="content">
            <h2>Plano Free</h2>
            <p>sdioujsfdnvpijusdnfgtpijbvn
              sdfgpjbnpdfgbndfghfghnfgdhnb
              dfasvsdfvsdfgbdfgbdfgbasdfvsdf
              gvdfgdbipjudfngipubn</p>
            <span>R$00,00</span>
          </div>
        </div>
        <div class="card">
          <div class="imgBx">
            <img src="https://conexoesdho.com/wp-content/uploads/2019/10/gold-icon.jpg">
          </div>
          <div class="content">
            <h2>Plano Gold</h2>
            <p>sdioujsfdnvpijusdnfgtpijbvn
              sdfgpjbnpdfgbndfghfghnfgdhnb
              dfasvsdfvsdfgbdfgbdfgbasdfvsdf
              gvdfgdbipjudfngipubn</p>
            <span>R$100,00/mês</span>
          </div>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import principal from "./components/principal.vue"
import carousel from "./components/Carrosel.vue"

export default {
  name: 'App',

  components: {
    principal,
    carousel,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
h1{
  position: relative;
}
.carrosel{
  width: 10%;
}

.container{
  position:relative;
  width: 1100px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  padding: 30px;
}

.container .card{
  position: relative;
  max-width: 300px;
  height: 215px;
  background: #368cb4;
  margin: 30px 10px;
  padding: 20px 15px;
  display: flex;
  flex-direction: column;
  box-shadow: 0px 5px 202px rgba(0,0,0,0.5);
  transition: 0.3s ease-in-out;
}

.container .card:hover{
  height: 420px;
}

.container .card .imgBx{
  position: relative;
  width: 160px;
  height: 130px;
  top: -60px;
  left: 45px;
  z-index: 1;
  box-shadow: 0px 5px 20px rgba(0,0,0,0.2);
}

.container .card .imgBx img{
  max-width: 100%;
  border-radius: 6px;
}

.container .card .content{
  position: relative;
  margin-top: -140px;
  padding: 10px 15px;
  text-align: center;
  color: #111;
  visibility: hidden;
  opacity: 0;
  transition: 0.3s ease-in-out;
}

.container .card:hover .content{
  visibility: visible;
  opacity: 1;
  margin-top: -10px;
  transition-delay: 0.03s;
}

.container .card .content span{
  font: bold;
  font-size: 200%;
}
</style>
