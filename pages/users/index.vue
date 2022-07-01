<template>
<div>
    <h2>User List</h2>

    <ul>
        <li v-for="user in users" :key="user.id">

        <!--to is important-->
        <nuxt-link :to="`/users/${user.id}`">{{user.id}}</nuxt-link>
        </li>
    </ul>
</div>
</template>

<script>
export default{
    name: "IndexUser",
    data() {
        return {
            
            users: [{id: 1}, {id: 2}, {id: 3}],
        }
    },
}
</script>