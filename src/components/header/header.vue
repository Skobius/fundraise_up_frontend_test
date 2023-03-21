<template>
    <header class="header">
        <div class="header__text">{{headerText}}</div>
        <div class="header__inner">
            <input-search></input-search>
            <simple-select></simple-select>
        </div>
    </header>
</template>

<style lang="scss" src="./header.scss"></style>

<script>
    import InputSearch from '../form-elements/input-search.vue'
    import SimpleSelect from '../form-elements/simple-select.vue'

    export default {
        name: 'Header',
        props: {
            
        },
        data() {
            return {
              headerText: 'Donations'  
            }
        },
        components: {
            InputSearch,
            SimpleSelect
        },
        methods: {
        }
    }
</script>