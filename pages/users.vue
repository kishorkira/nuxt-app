<template>
    <div>
       
        <input type="text" v-model="userId">
        <input type="button" @click="loadUser" value="load user">
        <nuxt-child></nuxt-child>

    </div>
</template>

<script>
export default {
    data(){
        return {
            userId : ''
        };
    },
    methods:{
        loadUser(){
            this.$router.push(`/users/${this.userId}`);
        }
    },
    layout : 'users'
}
</script>