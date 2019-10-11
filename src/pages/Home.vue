<template>
  <div>
    <Layout>
      <Typing>
        La Rueda del tiempo gira y las eras llegan y pasan y dejan tras de sí recuerdos que se convierten en
        leyenda. La leyenda se difumina, deviene mito, e incluso el mito se ha olvidado mucho antes de que la era que lo
        vio nacer retorne de nuevo. En una era llamada la tercera por algunos, una era que ha de venir, una era
        transcurrida hace mucho, comenzó a soplar un viento. El viento no fue el principio, pues no existen comienzos ni
        finales en el eterno girar de la Rueda del Tiempo. Pero aquél fue un principio.
      </Typing>
    </Layout>
    <Comic></Comic>
  </div>


</template>


<script>
  import Comic from '@/layout/Comic.vue';
  import Layout from '@/layout/Default.vue';
  import Typing from '@/components/Typing/Typing.vue';
  import SeoService from '../services/seoService';

  export default {
    name: 'home',
    components: {
      Layout,
      Typing,
      Comic
    },
    metaInfo() {
      let seoService = new SeoService({
        title: 'La Rueda del Tiempo',
        description: 'This is a description',
        image: 'this-is-image.png',
        richData: [
          {
            "@type": 'def',
            cdef: 'abc'
          }]
      });
      return seoService.getMetas();
    }
  };
</script>
