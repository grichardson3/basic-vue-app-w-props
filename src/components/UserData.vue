<template>
    <form v-on:submit.prevent="submitForm">
        <input v-model="nameInput" type="text" placeholder="name">
        <input v-model="ageInput" type="text" placeholder="age">
        <button>Submit</button>
    </form>
</template>

<script>
export default {
    data(){
        return {
            nameInput: '',
            ageInput: ''
        }
    },
    emits: [
        'update-info'
    ],
    methods: {
        submitForm(){
            this.$emit("update-info", this.nameInput, this.ageInput);
        }
    }
}
</script>
