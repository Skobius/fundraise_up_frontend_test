<template>
    <form class="form-block">
        <ul class="nav nav-tabs nav-justified">
            <li class="nav-item" v-for="(item, i) in tabs" :key="i">
                <a class="nav-link" @click.prevent="setActive(item.id)" :class="{ active: isActive(item.id) }" :href="'#' + item.id" >{{item.name}}</a>
            </li>
        </ul>
        <div class="tab-content py-3" id="myTabContent">
            <div class="tab-pane fade" :class="{ 'active show': isActive(item.id) }" :id="item.id" v-for="(item, i) in tabs" :key="i"><slot>{{item.content}}</slot></div>
        </div>
    </form>
</template>

<script>
    import BehaviorBlock from '../tabs/behavior.vue'

    export default {
        name: 'Infrormation-block',
        props: {
        },
        data() {
            return {
                activeItem: 'behavior',
                tabs: [
                    {name: 'Behavior', id: 'behavior', content: 'Behavior content'},
                    {name: 'Appearance', id: 'appearance', content: 'Appearance content'},
                    {name: 'Custom Fields', id: 'custom', content: 'Custom Fields content'},
                ]
            }
        },
        components: {
            BehaviorBlock
        },
        methods: {
            isActive (menuItem) {
                return this.activeItem === menuItem
            },
            setActive (menuItem) {
                this.activeItem = menuItem
            }
        }
    }
</script>