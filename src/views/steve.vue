<template lang="pug">
  .steve
    h1 QQQQQQQQQ
    a 123
</template>

<script>

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
  background: black

</style>