<template>
    <main class="main">
        <LeftBlock></LeftBlock>
        <RightBlock></RightBlock>
    </main>
</template>

<style lang="scss" src="./main.scss"></style>

<script>
    import RightBlock from '../right-block/right-block.vue'
    import LeftBlock from '../left-block/left-block.vue'

    export default {
        name: 'Main',
        props: {
            
        },
        data() {
            return {
                
            }
        },
        components: {
            RightBlock,
            LeftBlock
        },
        methods: {
        }
    }
</script>