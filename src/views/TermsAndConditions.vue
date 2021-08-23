<template>
  <div class="container">
  <div class="directory-entry">
      <div class="column-width-5">
  <img class="img-responsive lazy" src="g0v.png" alt="" style="float:left;margin:0px 10px"/>  
                  <h1>g0v.br</h1>
                    
    <p class="title">
                          <p>Toda vez que você vir o número zero no lugar da letra o, lembre-se de que é possível usar a internet e o modo de pensar digital (a linguagem binária, 0 e 1) para mudar o “gov” tradicional. <br />
Inspirados pelo g0v original, de Taiwan, com o qual, porém, não possuímos nenhum vínculo oficial, somos um movimento político, mas sem partido ou ideologia; defendemos a transparência dos governos e buscamos soluções inteligentes que facilitem e incentivem a participação popular nos assuntos da política, provendo os cidadãos de informações e poder para moldar a sociedade.<br />
O g0v.br é uma organização da sociedade civil que reúne pessoas dispostas a pôr a tecnologia a serviço do interesse público, desenvolvendo ferramentas que ampliem a capacidade dos brasileiros de monitorar as atividades realizadas pelo Estado -- em todas as suas esferas e poderes --, a fim de que, cada vez mais, o uso dos recursos públicos efetivamente atenda, e com eficiência, às necessidades e demandas da nação.
É uma comunidade livre e descentralizada, feita de pessoas que chegam com ideias novas e encontram outras pessoas dispostas a pôr essas ideias em prática. Todos os nossos projetos utilizam softwares open source e são desenvolvidos com trabalho voluntário. É de cidadãos para o bem público. <br />
Se você quer se tornar um apoiador ou parceiro do g0v.br, ou mesmo fazer parte desta comunidade, pode contribuir com seu trabalho, suas ideias, seu tempo, seu apoio financeiro. Saiba que a porta estará sempre aberta!
</p>                      </div>
                          <br />  <br />  <br />  <br />  <br />  <br />  <br />  <br />  <br />  <br />  <br />  <br /> 
      <div class="column-width-2"> 
              </div>
      <hr />
    </div>
  <div class="ldc-credits">
      <p style="text-align:center;" align="justify">
      <img src="g0v.png" alt="Logo">
      </p>
  </div>
    <h1>
      <StringFormatter :string="title" />
    </h1>
    <StringFormatter :string="abstract" />
  </div>
</template>
<script>
import { ServiceFactory } from "@/services/ServiceFactory.js";
import StringFormatter from "@/components/StringFormatter.vue";

const TermsService = ServiceFactory.get('terms');
export default {
  name: "TermsAndCond",
  components: {
    StringFormatter
  },
  data() {
    return {
      title: {},
      abstract: {}
    };
  },
  created() {
    const data = TermsService.getData();

    this.title = data.title;
    this.abstract = data.abstract;
  }
};
</script>
<style scoped>
.container {
  margin: 0px;
  padding-left: 1em;
  padding-right: 1em;
}
.container div {
  width: 100%;
  height: 100%;
}
</style>