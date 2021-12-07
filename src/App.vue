<template>
    <section>
        <active-user v-bind:username="nameInfo" v-bind:userage="ageInfo"></active-user>
        <user-data v-on:update-info="returnData"></user-data>
    </section>
</template>

<script>
export default {
    data(){
        return {
             nameInfo: 'Gareth Richardson',
             ageInfo: '25'
        }
    },
    methods: {
        returnData(name, age){
            this.nameInfo = name;
            this.ageInfo = age;
        }
    }
}
</script>
