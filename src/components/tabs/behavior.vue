<template>
    <div class="behavior tab-content">
        <div class="form-element">
            <div class="form-element__name">
                Designation
            </div>
            <div class="form-element__content">
                <CustomSelect
                :options="['Match Checkout Setting', 'Match Checkout Setting2', 'Match Checkout Setting3', 'Match Checkout Setting4']"
                :default="'Match Checkout Setting'"
                class="select"
                />
            </div>
        </div>
        <div class="form-element">
            <div class="form-element__name">
                Goal
            </div>
            <div class="form-element__content form-element__content--two-elements">
                <input type="text" class="custom-input">
                <CustomSelect
                :options="['USD', 'EUR', 'RUB']"
                :default="'USD'"
                class="select"
                />
            </div>
        </div>
        <div class="form-element">
            <div class="form-element__name form-element__name--top">
                Default Amount
            </div>
            <div class="form-element__content">
                <RadioBox label="Match Checkout Setting" value="Match Checkout Setting" v-model="MySelectedValue" />
                <RadioBox label="Customize" value="Customize" v-model="MySelectedValue" />
                <CheckBox label="Allow donor to change default currency" value="Allow donor to change default currency" v-model="MySelectedValues"  class="form-element__large-indentation"/>
            </div>
        </div>
        <div class="form-element form-element__block-indent">
            <div class="form-element__name form-element__name--top">
                Border size
            </div>
            <div class="form-element__content form-element__content--slider">
                <Slider v-model="borderSize" :min="0" :max="3" class="slider" />
                <span>{{ borderSize }}px</span>
            </div>
        </div>
        <div class="form-element">
            <div class="form-element__name form-element__name--top">
                Border radius
            </div>
            <div class="form-element__content form-element__content--slider">
                <Slider v-model="borderRadius" :min="0" :max="20" class="slider" />
                <span>{{ borderRadius }}px</span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" src="../form-elements/custom-select.scss"></style>
<style lang="scss" src="../form-elements/custom-radio.scss"></style>
<style lang="scss" src="../form-elements/custom-checkbox.scss"></style>
<style lang="scss" src="../form-elements/custom-slider.scss"></style>

<script>
    import CustomSelect from '../form-elements/custom-select.vue'
    import RadioBox from '../form-elements/custom-radio.vue'
    import CheckBox from '../form-elements/custom-checkbox.vue'
    import Slider from '../form-elements/custom-slider.vue'

    export default {
        name: 'behavior',
        props: {
        },
        data() {
            return {
                MySelectedValue: "Customize",
                MySelectedValues: '',
                borderSize: 2,
                borderRadius: 15,
            }
        },
        components: {
            CustomSelect,
            RadioBox,
            CheckBox,
            Slider
        },
        methods: {
        }
    }
</script>