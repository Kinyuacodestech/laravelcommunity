<template>
    <input class="border-gray-300 focus:border-primary-300 focus:ring focus:ring-primary-100 focus:ring-opacity-50 rounded-md shadow-sm" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" ref="input">
</template>

<script>
    import { defineComponent } from 'vue'

    export default defineComponent({
        props: ['modelValue'],

        emits: ['update:modelValue'],

        methods: {
            focus() {
                this.$refs.input.focus()
            }
        }
    })
</script>
