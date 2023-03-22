<template>
    <div class="information-block">
        <div class="information-block__inner">
            <div class="information-block__left">
                <div class="information-block__header">
                    <img src="images/dollar-sign.png" alt="dollar-sign">
                    Donation
                </div>
                <div class="information-block__cost">
                    <span class="information-block__usd">$20.60 USD</span>
                    <span class="information-block__eur">≈ €17.92 EUR</span>
                </div>
            </div>
            <div class="information-block__right">
                <span class="information-block__id">ID</span>
                <span class="information-block__number">TYNY694Y<img src="images/copy.png" alt="copy" class=""></span>
            </div>
        </div>
        <div class="information-block__status">
            <status-element
                v-for="(item, i) in listItems"
                :key="i"
                :item_data="item"
            >
            </status-element>
        </div>
    </div>
</template>

<style lang="scss" src="./left-block.scss"></style>

<script>
    import StatusElement from '../left-block/status-element.vue'

    export default {
        name: 'Infrormation-block',
        props: {
        },
        data() {
            return {
                listItems: [
                    {name:'Status', src: 'images/check.png', alt: 'check', text: 'Succeeded',},
                    {name:'Supporter', href: '#', link_name: 'Charlotte Ann'},
                    {name:'Campaign', href: '#', link_name: 'Heart walk'},
                ]
            }
        },
        components: {
            StatusElement
        },
        methods: {
        }
    }
</script>