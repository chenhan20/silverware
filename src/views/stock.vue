
<template lang="pug">
  .stock
    h1 {{ title }}
</template>

<script>

export default {
  name: "stock",
  data() {
    return {
      title: "steve的股票練習",
      count: 0
    };
  },
  methods: {
  },
  computed:{
  }
};
// @ is an alias to /src
</script>

<style scoped lang="scss">
$pc-media: 960px;
$phones-media: 480px;
// //電腦
@mixin pc-width() {
  @media all and (min-width: $pc-media) {
    @content;
  }
}
// //手機
@mixin phone-width() {
  @media all and (max-width: $phones-media) {
    @content;
  }
}
h1 {
  color: red;
}
</style>