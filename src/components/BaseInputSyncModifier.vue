<template>
  <input type="text" :value="text" @input="onInput" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputSyncModifier',
    props: {
        text: {
            type: String,
            value: ''
        }
    },
    methods: {
        onInput(event) {
            this.$emit('update:text', event.target.value)
        }
    }
}

</script>