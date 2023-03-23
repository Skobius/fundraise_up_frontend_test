<template>
    <div class="left-block">
        <information-block></information-block>
        <form-block></form-block>
    </div>
</template>

<style lang="scss" src="./left-block.scss"></style>


<script>
    import InformationBlock from '../left-block/information-block.vue'
    import FormBlock from '../left-block/form-block.vue'

    export default {
        name: 'LeftBlock',
        props: {
            
        },
        data() {
            return {
                
            }
        },
        components: {
            InformationBlock,
            FormBlock
        },
        methods: {
        }
    }
</script>