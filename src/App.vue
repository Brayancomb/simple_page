<template>
  <v-app> 
    <v-main>
      <v-container>
        <div class="logo" @click="goHome">
        <v-img src="./assets/Singular.png" width="30%" style="margin-rigth:10dp"></v-img>
        <h1 class="saudation">Saudações, Estudante...</h1>
        <h2 class="question">Diga-nos, para onde você quer ir hoje?</h2>
        </div>
      </v-container>

      <v-container class="superior">
          <div class="geral">
            <div class="card__container">
              <div class="card">
                <div class="card__content" @click="goBills">
                  <h3 class="card__header">Boleto</h3>
                  <img src="./assets/ic boleto.png" class="boleto">
                </div>
              </div>
              <div class="card">
                <div class="card__content" @click="goPortal">
                  <h3 class="card__header">Portal do Aluno</h3>
                  <img src="./assets/ic portal.png" class="portal">
                </div>
              </div>
            </div>
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
      location.href = "https://portal.bancomonetiza.com.br/app/consultar-boleto";
    },
    goPortal(){
      location.href = "https://portal.singulareducacional.com.br/rm/web/app/edu/portaleducacional/login/"
    },
    goHome(){
      location.href="https://www.singulareducacional.com.br/"
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
.card {
  width: 80%;
  height: 130%;
  max-height: 300px;
  padding: auto;
  text-align: center;
  background: #242426;
  border-radius: 30px;
  box-shadow: 10px 10px 25px #1b1c1b, -10px -10px 25px #2d302f;
  &__container {
    display: grid;
    width:100%;
    height:120%;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    align-items: center;
    justify-items: center;
    color: rgb(0, 0, 0);
  }
  &__content {
    width: 100%;
    height: 110%;
    background: whitesmoke;
    margin: 10px auto;
    border-radius: 30px;
    padding: 10px;
    cursor: pointer;
    transition: 0.3s all ease-in-out;
    &:hover{
      margin-top:-10px;
    }
  }
  &__header {
    text-transform: uppercase;
    font-size: 30px;
    margin: 30px auto;
  }
  .boleto{
    width: 150px;
  }
  .portal{
    width: 170px;
  }
  
}
</style>
