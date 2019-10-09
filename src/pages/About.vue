<template>
  <div class="about">
     About
  </div>
</template>

<script>
  import Layout from '@/layout/Default.vue';
  export default {
    name: 'default-layout',
    title() {
      return `Foo Page — ${this.someValue}`
    },
    data() {
      return {
        someValue: 'bar'
      }
    },
    components: {
      Layout
    }
  }

</script>
