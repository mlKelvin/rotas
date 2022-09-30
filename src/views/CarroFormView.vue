<template>
  <div>
    <h1>Form carros</h1>
    <p>{{$route.params.id}}</p>
    <button @click="voltar()">Voltar</button>
  </div>
</template>

<script>
export default {
    mounted(){
        console.log(this.$route.params.id)
    },
    methods: {
        voltar(){
            this.$router.go(-1)
        }
    }
}
</script>

<style>

</style>