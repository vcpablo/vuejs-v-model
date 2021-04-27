<template>
  <input type="text" :value="modelValue" @input="onInput" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputCustomMethod',
    props: {
        modelValue: {
            type: String,
            value: ''
        }
    },
    methods: {
        onInput(event) {
            this.$emit('update:modelValue', event.target.value)
        }
    }
}

</script>