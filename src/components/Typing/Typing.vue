<template>
  <div class="c-typing">
    {{this.message}}
  </div>
</template>
<style lang="scss">
  @import 'typing.scss';
</style>
<script>
  export default {
    props: ['toType'],
    data() {
      return {
        message: ''
      }
    },
    mounted() {
      const getSpeedByChar = (char) => {
        switch (char) {
          case '.':
          case '?':
            return 1500;
          case ',':
            return 750;
          case ' ':
            return 50;
          default:
            return 50;
        }
      };
      const typeWriter = (i) => {
        let text = this.toType;
        if (i < text.length) {
          this.message += text.charAt(i);
          setTimeout(() => {
              typeWriter(i + 1, text)
            }, getSpeedByChar(text.charAt(i))
          );
        }
      };
      typeWriter(0);
    }
  };
</script>
