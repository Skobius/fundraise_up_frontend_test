<template>
    <div class="right-block">
        <div class="right-block__element" v-for="(item, i) in menu" :key="i">
             <img :src="item.icon" :alt="item.alt" class="right-block__element-image">
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
                    { name: 'Change amount', icon: 'images/repeat.png', alt: 'repeat' },
                    { name: 'Change payment method', icon: 'images/wallet.png', alt: 'wallet' },
                    { name: 'Change date', icon: 'images/calendar.png', alt: 'calendar' },
                    { name: 'Cancel recurring', icon: 'images/x-circle.png', alt: 'x-circle' },
                ],
            }
        },
        methods: {
        }
    }
</script>