<template>
  <input type="text" v-model="model" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputPowerfulComputedProperty',
    props: {
        value: {
            type: String,
            value: ''
        }
    },
    computed: {
        model: {
            set(value) {
                this.$emit('input', value)
            },
            get() {
                return this.value
            }
        }
    }
}

</script>