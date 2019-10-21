
<template lang="pug">
  .steve
    h1 {{ title }}
    hr
    h3 count button(未使用vuex)  
    a count: {{count}}   
    button(@click="add") +
    button(@click="minus") -
    hr
    h3 count button(使用vuex)  
    a count: {{count}}   
    button(@click="increment") +
    button(@click="increment") -
</template>

<script>
import Vuex from 'vuex'

const store = new Vuex.Store({
  state: {
    count: 0
  },
  mutations: {
    increment (state) {
      state.count++
    }
  }
});


export default {
  name: "steve",
  data() {
    return {
      title: "steve的Vue練習",
      count: 0
    };
  },
  methods: {
    add() {
      this.count++;
    },
    minus() {
      this.count--;
    },
    increment () {
      store.commit('increment');
    }
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