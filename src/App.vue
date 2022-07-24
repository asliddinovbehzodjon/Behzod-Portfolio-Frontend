<template>

<div >
    <Main />
    <router-view />
</div>

</template>

<style lang="scss">
</style>

<script>

import Main from '@/views/Main.vue'

export default {
    name: "App",
    data() {
        return {
            
        };
    },
    mounted() {
       
    },

    components: {
        Main,
       

    }
}
</script>
