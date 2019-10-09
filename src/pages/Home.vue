<template>
  <Layout>
    <div class="home">
      Home
    </div>
  </Layout>
</template>


<script>
  import Layout from '@/layout/Default.vue';
  import SeoService from "../services/seoService";

  export default {
    name: 'home',
    components: {
      Layout
    },
    metaInfo() {
      let seoService = new SeoService({
        title: 'Home',
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
