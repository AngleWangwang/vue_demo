<template>
  <div v-cloak>
      <button v-on:click="btnclick">{{mes}}</button>
      <router-view></router-view>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mes:'LOGIN'
    }
  },
  methods: {
    btnclick() {
      if(this.mes=="LOGIN"){
        window.location.href="http://localhost:8080/#/"+"login";
        this.mes="REGISTER";
      }else{
        window.location.href="http://localhost:8080/#/"+"register";
        this.mes="LOGIN";
      }
    }
  }
};
</script>

<style>
  [v-cloak]{
    display: none;
  }
</style>