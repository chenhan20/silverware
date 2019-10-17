<template lang="pug">
  .steve
    h1 QQQQQQQQQ
    a 123
    h1 {{ title}}
</template>

<script>
export default {
  name: "steve",
  data() {
    return {
      title: "steve大哥"
    };
  }
};
// @ is an alias to /src
</script>

<style lang="sass">
$pc-media: 960px
$phones-media: 480px
//電腦
@mixin pc-width() 
  @media all and (min-width: $pc-media) 
    @content
//手機
@mixin phone-width() 
  @media all and (max-width: $phones-media) 
    @content

body
  background: #E7ECF3

</style>