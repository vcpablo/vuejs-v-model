<template>
  <input type="text" v-model="model" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputLocalVariableWatcher',
    props: {
        value: {
            type: String,
            value: ''
        }
    },
    data() {
        return {
            model: this.value
        }
    },
    watch: {
        model(currentValue) {
            this.$emit('input', currentValue)
        }
    }
}

</script>