<template>
    <div class="status-element">
        <div class="status-element__name">{{item_data.name}}</div>
        <div class="status-element__inner">
            <img :src="item_data.src" :alt="item_data.alt" v-if="item_data.src">
            <a :href="item_data.href" v-if="item_data.href" class="status-element__link">{{item_data.link_name}}</a>
            <span v-if="item_data.text">{{item_data.text}}</span>
        </div>
    </div>
</template>

<style lang="scss" src="./left-block.scss"></style>

<script>
    export default {
        name: 'Status-element',
        props: {
            item_data: {
                type: Object,
                default() {
                    return {}
                }
            }
        },
        data() {
            return {
            }
        },
        methods: {
        }
    }
</script>