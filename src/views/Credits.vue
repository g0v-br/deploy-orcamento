<template>
  <div class="container">
    <br /> 
    <h1> 
      Nossa Equipe:
    </h1>
    <br />
    <div class="views-row views-row-2 views-row-even clearfix">
    
<article class="node-765 node node-directory-listing clearfix">

      
        <div class="directory-entry">
      <div class="column-width-5">
  <img class="img-responsive lazy" src="gustavo.png" alt="" style="float:left;margin:0px 10px"/>  
                  <h2>Gustavo Pellegrini Dias</h2>
                    
    <p class="title">
      Voluntário de Orçamento do Gabinete da Vereadora Janaína Lima  </p>
                            <p class="email"><a href="mailto:gustavodias@uchicago.edu">gustavodias@uchicago.edu</a></p>
                          <p>Gustavo é um jovem paulistano de 20 anos. Ele cursa graduação em Economia e Ciência de Dados Geográficos na <br />Universidade de Chicago. Já foi assistente de pesquisa no Center for Spatial Data Science e redator no US COVID Atlas. <br />Atualmente, Gustavo é colaborador da RadicalxChange Foundation e voluntário no gabinete da vereadora Janaína Lima.</p>                      </div>
                          <br /> 
      <div class="column-width-2"> 
              </div>
      <hr />
    </div>

  
</article><!-- /.node -->
  </div>

  <div class="views-row views-row-2 views-row-even clearfix">
    
<article class="node-765 node node-directory-listing clearfix">

      
        <div class="directory-entry">
      <div class="column-width-5">
  <img class="img-responsive lazy" src="lucilene.png" alt="" style="float:left;margin:8px 10px"/>  
                  <h2>Lucilene Oshiro Corrêa</h2>
                    
    <p class="title">
      Assessora Parlamentar do Gabinete da Vereadora Janaína Lima    </p>
                            <p class="email"><a href="mailto:lucilene.oshiro@gmail.com ">lucilene.oshiro@gmail.com </a></p>
                          <p>Pós-graduada em Contabilidade Pública e servidora concursada da Prefeitura de São Paulo desde 2010, trabalhou na Secretaria da Fazenda nas áreas do Tesouro Municipal, <br />Planejamento e Orçamento e Assessoria Econômica. Foi Coordenadora do Orçamento e, posteriormente, Subsecretária de Planejamento e Orçamento. Participou de conselhos <br />fiscais em empresas do município de São Paulo e grupos de trabalho visando à eficiência do gasto público. Atualmente é assessora parlamentar da vereadora Janaína Lima <br />na Câmara Municipal de SP.</p>                      </div>
      <div class="column-width-2"> 
              </div>
      <hr />
    </div>

  
</article><!-- /.node -->
  </div>

  <div class="views-row views-row-2 views-row-even clearfix">
    
<article class="node-765 node node-directory-listing clearfix">

      
        <div class="directory-entry">
      <div class="column-width-5"> <br /> 
  <img class="img-responsive lazy" src="vitor.png" alt="" style="float:left;margin:0px 10px"/> 
                  <h2>Vitor Theodoro Carboni</h2>
                    
    <p class="title">
      Voluntário de Orçamento do Gabinete da Vereadora Janaína Lima   </p>
                            <p class="email"><a href="mailto:vitheodorocarboni@gmail.com ">vitheodorocarboni@gmail.com</a></p>
                          <p> Vitor é um jovem paulistano de 21 anos nascido e criado no Parque Santa Madalena, bairro da periferia da cidade de São Paulo, ele é estudante de Economia no Insper, colaborador do <br /> Observatório da Revisão do Plano Diretor (localizado na mesma instituição), voluntário no gabinete da vereadora por São Paulo Janaína Lima e atualmente trabalha na elaboração <br />conjunta de uma Revisão de Literatura Acadêmica no tema Plano Diretor.</p>                      </div> <br /> 
      <div class="column-width-2"> 
              </div>
      <hr />
    </div>

<p> <br /> Nossos agradecimentos à equipe <a
          href="https://github.com/g0v-it"
        >G0v.it</a> que desenvolveu a versão original do código deste site: Miah Mohd Ehtesham, Leonardo Longhi, Yassine Ouahidi e Enrico Fagnoni.
<br /> <br /> 
Foram utilizados os seguintes componentes open source para este projeto:
<br /> <br /> 
- <a
          href="https://d3js.org/"
        >D3.js library</a> <br /> 
- <a
          href="https://vuejs.org"
        >Vue javascript framework</a> <br /> 
- <a
          href="https://github.com/linkeddata/rdflib.js"
        >rdflib project</a> by TimBL & LinkedData team <br /> 
- <a
          href="https://github.com/solid/solid-spec"
        >SOLID</a> specifications
</p>
  
</article><!-- /.node -->
  </div>
    <StringFormatter :string="abstract"/>
    <!-- Warning: removing or changing the following statement breaks the LODMAP2D license -->
    <div class="ldc-credits">
      <p>
        This application includes the
        <a
          href="https://github.com/linkeddatacenter/LODMAP2D"
        >LODMAP2D software</a> developed by
        <a href="http://LinkedData.Center/"><img src="favicon-32x32.png"  height="32" width="32"> LinkedData.Center</a> and contributors.
      </p>
    </div>
  </div>
</template>
<script>
import { ServiceFactory } from "@/services/ServiceFactory.js";
import StringFormatter from "@/components/StringFormatter.vue";

const CreditsService = ServiceFactory.get("credits");
export default {
  name: "Credits",
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
    const data = CreditsService.getData();

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
.ldc-credits {
  margin-left: auto;
  margin-top: 1em;
  font-style: italic;
  color: rgba(100, 100, 100, 1);
}
</style>