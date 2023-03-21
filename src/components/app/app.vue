<template>
  <div class="todo-app">
    <Header></Header>
    <Main></Main>
  </div>
</template>

<style lang="scss" src="./app.scss"></style>

<script>
    import Header from '../header/header.vue'
    import Main from '../main/main.vue'

    export default {
        name: 'App',
        data() {
            return {
          
            }
        },
        watch: {
        },
        mounted: function () {
        },
        components: {
            Header,
            Main
        },
        created() {
        }
    }

</script>