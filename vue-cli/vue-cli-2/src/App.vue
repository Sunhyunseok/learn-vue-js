<template>
  <!-- template root는 하나의 최상위 element만 있어야함 -->
  <div>
    <!-- v-vind:하위컴포넌트에서 프롭스 속성이름="상위컴포넌트 데이터 이름" -->
    <app-header 
    v-bind:propsdata="str"
    v-on:renew="renewStr"
    ></app-header>
  </div>
</template>

<script>
//기존 방식
// new Vue({
//   data: {
//     str: 'hi'
//   }
// })
// cli를 통해 프로젝트를 만들면 export 안의 속성은 function 함수로 연결해서 
// return으로 새로운 객체를 반환해주는 형식으로 작성헤야함

import AppHeader from './components/AppHeader.vue';

export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header':AppHeader
  },
  methods: {
    renewStr: function(){
      this.str= 'hi';
    }
  }
}
</script>

<style>

</style>