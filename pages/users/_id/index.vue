<template>
<div>
    <h2>singel user with id : {{$route.params.id}}</h2>
    <nuxt-link to="/users">go back</nuxt-link>
</div>
</template>

<script>
export default {
    validate(data){       
        return  /^\d+$/.test(data.params.id);
    },
    layout : 'users'
}
</script>


