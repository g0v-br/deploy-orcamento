<template>
  <div class="container">
  <div class="directory-entry">
      <div class="column-width-5">
  <br /> <br />  <p style="font-size: 20px; text-align: center" class="title">
                     SOBRE O OBSERVATÓRIO  </p> <br />
  <img class="img-responsive lazy" src="preview.png" alt="" style="float:left;margin:0px 25px"/>  
                    
   <p align="justify">   
                     O Observatório do Orçamento de São Paulo foi inspirado num projeto desenvolvido por integrantes do movimento g0v de Taiwan que se trata de uma plataforma digital bastante interativa por meio da qual os cidadãos taiwaneses podem monitorar a execução do orçamento público do governo a partir de diversas perspectivas -- tendências temporais, comparações entre diferentes departamentos da administração, opinião pública e detalhamento da composição das receitas.    <br /> <br /> 
É verdade que os cidadãos paulistanos já dispõem de uma plataforma digital onde podem acessar livremente informações sobre o orçamento do município de São Paulo: conforme o Decreto Municipal nº 53.623/12, que regulamenta a Lei de Acesso à Informação (Lei Federal 12.527/11), a Prefeitura criou em 2012 o Portal da Transparência – SP para ser o principal veículo de disponibilização ativa de dados e informações acerca da administração pública. Porém o Portal é deficiente na comunicação com o cidadão, pois exige certa familiaridade com termos mais técnicos presentes nas informações prestadas e se vale de mecanismos de busca e recursos visuais que tornam a exibição de conteúdo pouco intuitiva e interativa (em vista do que é possível fazer como alternativa). Essa deficiência poderia ser tratada com atualizações do Portal, e qualquer pessoa consegue entrar em contato para enviar sugestões de melhorias. No entanto, não existe uma agenda de atualizações divulgada, nem é possível quão devidamente consideradas são as sugestões enviadas pelos usuários.<br /> <br /> 
          Ao contrário do Portal da Transparência – SP, o Observatório do Orçamento de São Paulo não pertence ao governo, mas possui o selo g0v.br. Portanto, seu gerenciamento, além de não estar sujeito a influências de natureza eleitoral, consegue ser mais ágil para lidar com a manutenção da plataforma e está sempre aberto a desenvolvedores e quaisquer outros cidadãos ou organizações que queiram contribuir de alguma forma, seja enviando sugestões de novos conteúdos para serem exibidos na plataforma ou dicas para melhorar a qualidade da própria exibição (as contribuições serão devidamente consideradas), seja tornando-se apoiadores, colaboradores, parceiros etc. do g0v.br.<br /> <br /> 
          O que dá lugar ao Observatório não é a carência de um portal de divulgação de dados públicos com transparência, mas de um portal que, além de transparente, constantemente procura facilitar a busca e a localização de informações públicas com o uso de recursos de exibição intuitivos e interativos e um visual agradável ao usuário, pois é assim que acreditamos que podemos incentivar o engajamento cívico dos paulistanos e ampliar a sua capacidade de supervisionar o governo e avaliar se o uso das dezenas de milhões de reais arrecadadas todos os anos tem servido adequadamente a cidade.

</p>                      </div>
                          <br />  
      <div class="column-width-2"> 
              </div>
      <hr />
    </div>
    <div class="directory-entry">
      <div class="column-width-5">
  <br />  <p style="font-size: 20px; text-align: center" class="title">
                     SOBRE O G0V.BR </p> <br /> 
  <img class="img-responsive lazy" src="g0v.png" alt="" style="float:left;margin:0px 0px"/>  
                    
   <p align="justify">   
  Toda vez que você vir o número zero no lugar da letra o, lembre-se de que é possível usar a internet e o modo de pensar digital (a linguagem binária, 0 e 1) para mudar o “gov” tradicional. Inspirados pelo g0v original, de Taiwan, com o qual, porém, não possuímos nenhum vínculo oficial, somos um movimento político, mas sem partido ou ideologia; defendemos a transparência dos governos e buscamos soluções inteligentes que facilitem e incentivem a participação popular nos assuntos da política, provendo os cidadãos de informações e poder para moldar a sociedade.<br /> <br /> 
O g0v.br é uma organização da sociedade civil que reúne pessoas dispostas a pôr a tecnologia a serviço do interesse público, desenvolvendo ferramentas que ampliem a capacidade dos brasileiros de monitorar as atividades realizadas pelo Estado -- em todas as suas esferas e poderes --, a fim de que, cada vez mais, o uso dos recursos públicos efetivamente atenda, e com eficiência, às necessidades e demandas da nação.
É uma comunidade livre e descentralizada, feita de pessoas que chegam com ideias novas e encontram outras pessoas dispostas a pôr essas ideias em prática. Todos os nossos projetos utilizam softwares open source e são desenvolvidos com trabalho voluntário. É de cidadãos para o bem público. 
Se você quer se tornar um apoiador ou parceiro do g0v.br, ou mesmo fazer parte desta comunidade, pode contribuir com seu trabalho, suas ideias, seu tempo, seu apoio financeiro. Saiba que a porta estará sempre aberta! <br /> <br /> <br /> <br />
</p>                      </div>
                          
      
      <hr />
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