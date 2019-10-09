<template>
  <div>
    <HeaderDefault />
    <slot />
    <FooterDefault/>
  </div>
</template>


<script>
  import HeaderDefault from '@/components/Header/Default.vue';
  import FooterDefault from '@/components/Footer/Default.vue';
  export default {
    name: 'default-layout',
    components: {
      HeaderDefault,
      FooterDefault,
    }
  }
</script>
