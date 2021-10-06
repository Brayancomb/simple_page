<template>
  <v-app> 
    <v-main>
      <v-container>
        <div class="logo" >
        <v-img id="se" src="./assets/Singular.png" width="30%" style="margin-rigth:10dp" @click="goHome"></v-img>
        <h1 class="saudation">Saudações, Estudante...</h1>
        <h2 class="question">Diga-nos, para onde você quer ir hoje?</h2>
        </div>
      </v-container>

      <v-container>
          <div class="geral" style="display:flex; flex-direction:row; flex-wrap: nowrap; align-conten: center; justify-content: center; align-items: center;">
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
html {
    overflow: scroll;
    overflow-x: hidden;
}
::-webkit-scrollbar {
    width: 0px;  /* Remove scrollbar space */
    background: transparent;  /* Optional: just make scrollbar invisible */
}

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
  width: 60%;
  height: 80%;
  max-height: 300px;  
  padding: auto;
  text-align: center;
  //background: #242426;
  border-radius: 30px;
  //box-shadow: 5px 5px 5px #1b1c1b, -5px -5px 5px #2d302f;
  &__container {
    display: flex;
    width:60%;
    height: 60%;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    justify-items: center;
    color: rgb(0, 0, 0);
    
  }
  &__content {
    // box-shadow: -5px -5px 5px #444444;
    width: 90%;
    height: 90%;
    background: whitesmoke;
    margin: 10px auto;
    border-radius: 30px;
    padding: 20px;
    cursor: pointer;
    transition: 0.3s all ease-in-out;
    &:hover{
      margin-top:-40px;
      border-style: solid;
      border-color:  #00A2FF;
    }
  }
  &__header {
    text-transform: uppercase;
    font-size: 30px;
    margin: 5px auto;
  }
  .boleto{
    width: 150px;
  }
  .portal{
    width: 170px;
  }
  
}
</style>
