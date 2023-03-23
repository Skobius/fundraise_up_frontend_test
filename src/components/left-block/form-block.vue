<template>
    <form class="form-block">
        <div class="tabs-menu-inner">
            <div class="tabs-menu">
                <div
                    v-for="(tab, i) in tabs"
                    :key="i"
                    :class="['tabs-menu__item', { active: currentTab === tab.id }]"
                    @click="currentTab = tab.id"
                >
                    {{ tab.name }}
                </div>
            </div>
        </div>
        <component :is="currentTab" class="tab-content"></component>
        <div class="form-block__footer">
            <button class="btn btn--success">Save changes</button>
            <button class="btn btn--default">Cancel</button>
        </div>
    </form>
</template>

<script>
    import behavior from '../tabs/behavior.vue'
    import appearance from '../tabs/appearance.vue'
    import custom from '../tabs/custom.vue'
    import questions from '../tabs/questions.vue'
    import url from '../tabs/url.vue'

    export default {
        name: 'InfrormationBlock',
        props: {
        },
        data() {
            return {
                currentTab: 'behavior',
                tabs: [
                    {name: 'Behavior', id: 'behavior'},
                    {name: 'Appearance', id: 'appearance'},
                    {name: 'Custom Fields', id: 'custom'},
                    {name: 'Questions', id: 'questions'},
                    {name: 'URL Control', id: 'url'},
                ]
            }
        },
        components: {
            behavior,
            appearance,
            custom,
            questions,
            url
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