<template>
  <div>
    <AppHeader v-bind:propsdata="str" v-on:renew="renewStr"></AppHeader>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader'

export default {
  data: function() { // 다른 컴포넌트들과 충돌하면 안되기 때문에 함수화
    return {    
      str : 'Header'
    }
  },
  components: {
    AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'HELLO';
    }
  }
}
</script>

<style>

</style>