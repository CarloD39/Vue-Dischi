<template>
    <div>
        {{poster}}
        {{title}}
        {{author}}
    </div>
</template>



<script>
export default {
    name:'albumMusic',
    props: {
        poster: String,
        title: String,
        author: String,
    }
}
</script>


<style lang="scss" scoped>

</style>