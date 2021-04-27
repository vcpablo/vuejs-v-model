<template>
  <input type="text" :value="value" @input="onInput" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputCustomMethod',
    props: {
        value: {
            type: String,
            value: ''
        }
    },
    methods: {
        onInput(event) {
            this.$emit('input', event.target.value)
        }
    }
}

</script>