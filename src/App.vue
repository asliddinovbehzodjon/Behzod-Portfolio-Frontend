<template>
<div>
 <Main />
</div>
<router-view />
</template>

<style lang="scss">
</style>

<script>
import Main from '@/views/Main.vue'

export default {
    name: 'App',
    components: {
    Main,
   
}
}
</script>
