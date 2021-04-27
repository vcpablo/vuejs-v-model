<template>
  <input type="text" :value="text" @input="onInput" placeholder="Type something..." />
</template>

<script>
export default {
    name: 'BaseInputCustomPropAndEvent',
    model: {
        prop: 'text',
        event: 'update'
    },
    props: {
        text: {
            type: String,
            value: ''
        }
    },
    data() {
        return {
            model: this.value
        }
    },
    methods: {
        onInput(event) {
            this.$emit('update', event.target.value)
        }
    }
}

</script>