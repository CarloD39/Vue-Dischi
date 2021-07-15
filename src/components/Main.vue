<template>
    <div>
        <albumMusic v-for="(albumMusic, index) in albumsMusic" :key='index' 
        :poster="albumMusic.poster"
        :title="albumMusic.title"
        :author="albumMusic.author"
        />
    </div>
</template>



<script>

import albumMusic from './albumMusic.vue'

export default {
    name:'Main',
    components: {
        albumMusic
    },

    props: {
        albumsMusic: Array
    }
}
</script>


<style lang="scss" scoped>

</style>