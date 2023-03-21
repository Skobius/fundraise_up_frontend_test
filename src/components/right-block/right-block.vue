<template>
    <div class="right-block">
        <div class="right-block__element" v-for="(item, i) in menu" :key="i">
             <img :src="item.icon" alt="serch" class="right-block__element-image">
             <div class="right-block__element-text">{{item.name}}</div>
        </div>
    </div>
</template>

<style lang="scss" src="./right-block.scss"></style>

<script>
    export default {
        name: 'Right-block',
        props: {
            
        },
        data() {
            return {
                menu: [
                    { name: 'Change amount', icon: 'images/repeat.png' },
                    { name: 'Change payment method', icon: 'images/wallet.png' },
                    { name: 'Change date', icon: 'images/calendar.png' },
                    { name: 'Cancel recurring', icon: 'images/x-circle.png' },
                ],
            }
        },
        methods: {
        }
    }
</script>