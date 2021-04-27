<template>
  <input type="text" v-model="model" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputPowerfulComputedProperty',
    props: {
        modelValue: {
            type: String,
            value: ''
        }
    },
    computed: {
        model: {
            set(value) {
                this.$emit('update:modelValue', value)
            },
            get() {
                return this.modelValue
            }
        }
    }
}

</script>