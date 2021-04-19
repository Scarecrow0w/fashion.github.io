<template>
    <div class="flex flex-col items-center text-center side-info-container">
        <div class="flex flex-col items-center justify-center w-full about-author-container">
            <div class="flex items-center justify-center w-full h-12 mb-5 font-serif border">
                <span>About the author</span>
            </div>
            <div class="flex flex-col shadow-md about-author hover:shadow-2xl">
                <img class="w-full" src="../assets/img/author.png" alt="author-img">
                <div class="flex flex-col justify-between flex-1 author-info">
                    <h3 class="font-serif">Kate Willems</h3>
                    <i class="font-serif text-sm">Food & cooking bloger</i>
                    <span class="text-sm">Hi, I'm Sonia. Cooking is the way I express my creative side to the world. Welcome to my Kitchen Corner on...</span>
                </div>
                <div class="flex items-center justify-center w-full h-10 border-t"><span class="font-serif text-xs uppercase text-tgold">continue reading</span></div>
            </div>
        </div>

        <div class="flex flex-col w-full">
            <div class="flex items-center justify-center w-full h-12 mb-5 font-serif border">
                <span>Featured posts</span>
            </div>
            <div 
            class="flex flex-col w-full shadow-md post-card hover:shadow-2xl"
            v-for="post in posts" 
            :key="post.id">
                <img :src="post.img" alt="post-img">
                <div class="flex flex-col items-center justify-between h-full card-content">
                    <h3 class="text-xs uppercase text-tgold">{{ post.title }}</h3>
                    <p class="font-serif text-lg">{{ text }}</p>
                    <p class="flex justify-between w-40 font-serif text-xs text-gray-500"><span>{{ date }}</span><span class="text-gray-400">By <span class="text-gray-500">{{ author }}</span></span></p>
                </div>
            </div>
        </div>

        <div class="flex flex-col w-full mt-10 font-serif">
            <div class="flex items-center justify-center h-12 border">Categories</div>
            <div class="flex flex-col categories">
                <div 
                class="flex items-center justify-between flex-1 text-sm border-b category"
                v-for="category in categories" 
                :key="category.id">
                    <span class="cursor-pointer hover:underline">{{ category.title }}</span>
                    <span>({{ category.quantity }})</span>
                </div>
            </div>
        </div>

        <div class="flex flex-col w-full mt-16 font-serif">
            <div class="flex items-center justify-center h-12 mb-5 border">Social media</div>
            <div class="flex flex-wrap justify-between w-full socials">
                <div 
                class="flex flex-col items-center justify-between cursor-pointer social hover:bg-gray-200"
                v-for="social in socials" 
                :key="social.id">
                    <i :class="social.icon" class="text-xl"></i>
                    <span>{{ social.quantity }}</span>
                    <span>{{ social.type }}</span>
                </div>
            </div>
        </div>

        <div class="flex flex-col w-full font-serif tags-container">
            <div class="flex items-center justify-center w-full h-12 border">Tags</div>
            <div class="flex flex-wrap justify-between w-full mt-5 tags">
                <div 
                class="flex items-center justify-center cursor-pointer tag hover:bg-gray-200"
                v-for="tag in tags" 
                :key="tag.id">
                    <span>{{ tag }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import socials from '/src/socials'

export default {
    data() {
        return {
            posts: {
                jeans: {
                    title: 'jeans',
                    img: '../src/assets/img/jeans.png'
                },
                city: {
                    title: 'city',
                    img: '../src/assets/img/city.png'
                },
                photography: {
                    title: 'photography',
                    img: '../src/assets/img/photography.png'
                }                
            },
            text: "One of Saturn's largest rings may be newer than anyone",
            date: 'June 6, 2019',
            author: 'Rickie Baroch',
            categories: {
                fashion: {
                    title: 'Fashion',
                    quantity: 23
                },
                style: {
                    title: 'Style & clothes',
                    quantity: 7
                },
                minimalism: {
                    title: 'Minimalism',
                    quantity: 16
                },
                blacknwhite: {
                    title: 'Black & White',
                    quantity: 5
                },
                modern: {
                    title: 'Modern clothes',
                    quantity: 12
                }
            },
            socials: socials,
            tags: ['Business', 'Freelance', 'Money', 'Experience', 'Lifestyle', 'SEO', 'Wordpress', 'Marketing', 'UX', 'Modern', 'Success', 'Nature']
        }
    },
}
</script>

<style scoped>
    .side-info-container {
        width: 270px;
        margin-left: 130px;
    }  

    .about-author-container {
        margin-bottom: 70px;
    }

    .about-author {
        height: 385px;
    }

    .author-info {
        padding: 14px 20px;
    }

    .about-author img {
        height: 180px;        
        object-fit: cover;
    }

    .post-card {
        height: 287px;
        margin-bottom: 30px;
    }

    .card-content {
        padding: 14px 10px;
    }

    .post-card img {
        object-fit: cover;
        width: 100%;
        height: 160px;
        filter: contrast(0.8);
    }  

    .categories {
        height: 235px;
    }  

    .category span {
        color: #666;
    }

    .category:last-child {
        border-bottom: none;
    } 

    .socials {
        height: 270px;
    }

    .social {
        width: 88px;
        height: 88px;
        background: #f8f9fa;
        padding: 17px 0 13px 0;
    }

    .social span {
        color: #999;
        font-size: 12px;
    }

    .social i {
        color: #5a5a5a;
    }

    .tags-container {
        margin-top: 70px;
    }

    .tags {
        height: 150px;
    }

    .tag {
        background: #f8f9fa;
        height: 30px;
        padding: 6px 15px;
    }
</style>