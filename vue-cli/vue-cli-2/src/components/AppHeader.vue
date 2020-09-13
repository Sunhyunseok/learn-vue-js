<template>
  <header>
      <h1>{{propsdata}}</h1>
      <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
    props: ['propsdata'],
    methods: {
        sendEvent: function() {
            //renew 라는 이벤트 보내기
            this.$emit('renew');
        }
    }

}
</script>

<style>

</style>