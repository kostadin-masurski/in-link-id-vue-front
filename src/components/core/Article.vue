<template>
    <div>
        <div v-for="(article, index) in Articles.allArticles" :key="article.id"
        @click="selectArticle(index)" :class="{active: index === selectedArticleIndex, 'article-container': true}">
            <h3>{{article.author}}</h3>
            <h4>{{article.title}}</h4>
            <div>
                <p>
                    {{article.content.substring(0, article.content.indexOf(' ', 150))}} ... 
                    <span @click="readMore">read more</span>
                </p>
                <p style="display: none">
                    {{article.content}}
                    <span @click="readLess"> read less</span>
                </p>
            </div>
            <img :src="article.imgUrl" alt="Article image">
            <p><a :href="article.link" class="btn btn-primary">More Info</a></p>
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
        return {
            Articles,
            selectedArticleIndex: 0
        };
    },
    methods: {
        selectArticle(idx){
            this.selectedArticleIndex = idx;
            console.log('article ' + this.showMore);
            this.$emit('readMore', idx);
        },
        readMore(ev){
            ev.target.parentNode.style.display = 'none';
            ev.target.parentNode.nextSibling.style.display = 'block';
        },
        readLess(ev){
            ev.target.parentNode.style.display = 'none';
            ev.target.parentNode.previousSibling.style.display = 'block';
        }
    },
    computed: {
        showMore(){
            return this.Articles.allArticles[this.selectedArticleIndex].author;
        }
    }
}
</script>

<style scoped>
    p{
        margin: 3px;
    }
    span{
        color: deepskyblue;
        cursor: pointer;
    }
    img{
        width: 98%;
    }
    .article-container{
        width: 40%;
        padding: 1%;
        margin-left: 5%;
        margin-right: 5%;
    }
    .active{
        background-color: lightgray;
    }
</style>