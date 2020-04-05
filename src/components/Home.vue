<template>
    <div>
        <home-article @readMore="readMoreHandler($event)"></home-article>
    </div>
</template>

<script>
import HomeArticle from './core/Article.vue'

export default {
    name: 'Home',
    components: {
        HomeArticle
    },
    methods: {
        readMoreHandler(i) {
            console.log('in home ' + i);
            console.log('in home ' + i);
        }
    }
}
</script>

<style scoped>

</style>