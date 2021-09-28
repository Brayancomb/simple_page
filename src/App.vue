<template>
  <v-app> 
    <v-main>
      <v-container>
        <div class="logo">
        <v-img src="./assets/Singular.png" width="30%" style="margin-rigth:10dp"></v-img>
        <h1 class="saudation">Saudações, Estudante...</h1>
        <h2 class="question">Diga-nos, para onde você quer ir hoje?</h2>
        </div>
      </v-container>

      <v-container>
        <div>
          <v-row dense justify="space-between" >
            <v-col
              lg="3"
              class=" pa-2 mt-5 mb-8"
            >
              <v-card
                outlined
                tile
                @click="goBills"
                style="text-align: -webkit-center;"
              >
                <v-card-title style="font-size: 45px; place-content: center;">Boleto</v-card-title>
                <v-img src="./assets/ic boleto.png" width="300px"></v-img>
              </v-card>           
            </v-col>
            <v-col
              lg="3"
              class="pa-2 mt-5 mb-8"
            >
              <v-card
                outlined
                tile
                style="text-align: -webkit-center;"
                @click="goPortal"
              >
                <v-card-title style="font-size: 40px; place-content: center;">Portal do Aluno</v-card-title>
                <v-img src="./assets/ic portal.png" width="330px"></v-img>
              </v-card>           
            </v-col>
          </v-row>
        </div>   
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
/// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    //
  }),
  methods:{
    goBills(){
      location.href = "https://www.youtube.com/results?search_query=clicable+v-card";
    },
    goPortal(){
      location.href = "https://www.facebook.com/?ref=logo"
    }
    
  }
};
</script>
<style lang="scss">
main{
  background-image: url(./assets/Background.png);
  background-size: 100%;
}
.logo{
  text-align: -webkit-center;
  margin-top: 30px;
}
.saudation{
  color: aqua;
  font-size: 50px;
  margin-top: 20px;
}
.question{
  color: white;
  font-size: 40px;
  margin-top: 10px;
}
</style>
