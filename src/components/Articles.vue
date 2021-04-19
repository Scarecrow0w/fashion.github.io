<template>
    <div class="flex flex-col items-center articles-container">
        <div class="flex flex-wrap justify-between font-serif articles">
            <div 
            class="flex flex-col items-center text-center shadow-md article-card hover:shadow-2xl "
            v-for="article in articles" 
            :key="article.ID">
                <img :src="article.picture" alt="article-picture">
                <div class="flex flex-col justify-between flex-1 article-info">
                    <h2 class="">{{ article.name }}</h2>
                    <span class="text-xs">{{ article.desc }}</span>
                    <span class="text-xs">{{ article.date_create.slice(0, 10) }}</span>
                </div>
            </div>
        </div>
        <div class="flex items-center justify-between text-sm border articles-navigation">
            <span class="text-gray-400 uppercase">&#60; older post</span>
            <span class="cursor-pointer text-tgold hover:text-tgold">1</span>
            <span class="cursor-pointer hover:text-tgold">2</span>
            <span class="cursor-pointer hover:text-tgold">3</span>
            <span>...</span>
            <span class="cursor-pointer hover:text-tgold">8</span>
            <span class="uppercase cursor-pointer hover:text-tgold">next post &#62;</span>
        </div>
    </div>
</template>

<script>
  import axios from 'axios'
  export default {

    data() {
      return {
        articles: null
      }
    },

    // computed: {
    //     dateFormatted() {

    //     }
    // },

    mounted() {
      axios.get('https://emi-shop.ru/uploads/news.json').then((response) => {
        console.log(response.data);
        this.articles = response.data
      })
    },

  }  
</script>
    
<style scoped>
    .articles-container {
        width: 770px;
        margin-left: 20%;
    }

    .article-card {
        width: 370px;
        height: 411px;
        margin-bottom: 30px;
    }

    .article-info {
        padding: 10px 20px 5px 20px;
    }

    .article-card img {
        height: 280px;
        width: 100%;
        object-fit: cover;
    }

    .article-card h2 {
        font-size: 20px;
        line-height: 28px;
    }

    .article-card span {
        color: #666;
    }  

    .articles-navigation {
        width: 509px;
        height: 50px;
        padding: 0 25px;
    }
</style>