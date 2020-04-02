<template>
    <div>
        <div v-for="article in Articles.allArticles" :key="article.id" class="article-container">
            <h3>{{article.author}}</h3>
            <div>
                <textarea v-text="article.content" rows="4" cols="68"></textarea>
            </div>
            <img :src="article.imgUrl" width="500" alt="Article image">
            <p><a :href="article.link">More Info</a></p>
            <hr/>
        </div>
    </div>
</template>

<script>
import Articles from '../../services/article.service.json'

export default {
    name: 'Article',
    props: {
        articles: Array,
        author: String,
        content: String,
        imgUrl: String,
        link: String,
    },
    data() {
        return {Articles}
    }
}
</script>

<style scoped>
    
</style>