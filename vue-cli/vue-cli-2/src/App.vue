<template>
  <!-- template root는 하나의 최상위 element만 있어야함 -->
  <div>
    {{str}}
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
export default {
  data: function() {
    return {
      str: 'hi'
    }
  }
}
</script>

<style>

</style>