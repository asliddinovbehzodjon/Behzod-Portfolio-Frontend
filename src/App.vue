<template>

<div >
    <Main />
    <router-view :key="$route.fullPath" />
</div>


</template>

<style lang="scss">
</style>

<script>

import Main from '@/views/Main.vue'

export default {
    name: "App",
    components: {
        Main,
       

    }
}
</script>
