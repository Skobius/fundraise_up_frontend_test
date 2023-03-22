<template>
    <div class="simple-select">
        <select name="simpleSelect" class="simple-select__inner">
            <option :value="item.value" v-for="(item, i) in option" :key="i">{{item.name}}</option>
        </select>
    </div>
</template>

<style lang="scss" src="./form-elements.scss"></style>

<script>

    export default {
        name: 'SimpleSelect',
        props: {
            
        },
        data() {
            return {
                option: [
                    {name: 'All statuses', value:''},
                    {name: 'status 1', value:''},
                    {name: 'status 2', value:''},
                    {name: 'status 3', value:''},
                ]
            }
        },
        methods: {
        }
    }
</script>