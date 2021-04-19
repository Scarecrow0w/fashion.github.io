<template>
    <footer class="flex flex-col items-center ">
        <div class="logo">
            <span class="font-serif text-2xl font-bold">FASHION</span>
            <div class="relative w-full border border-transparent bg-fgold opacity-30 logo-line"></div>
        </div>

        <div class="flex items-center justify-between text-sm links">
            <span class="cursor-pointer hover:text-fgold text-fgold">Home</span>
            <span class="cursor-pointer hover:text-fgold">Recipes</span>
            <span class="cursor-pointer hover:text-fgold">Article</span>
            <span class="cursor-pointer hover:text-fgold">Contact</span>
            <span class="cursor-pointer hover:text-fgold">Purchase</span>
        </div>

        <div class="flex items-center justify-between footer-socials">
            <div 
            class="flex items-center justify-center border rounded-full cursor-pointer hover:bg-tgold footer-socials-icon"
            v-for="icon in icons" 
            :key="icon.id">
                <i :class="icon"></i>
            </div>
        </div>
        <hr class="mt-10">
        <span class="text-sm rights">@2019 Logwork. All Right Reserved.</span>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            icons: ['fab fa-facebook-f', 'fab fa-twitter', 'fab fa-pinterest-p', 'fab fa-google-plus-g', 'fab fa-behance', 'fab fa-instagram']
        }
    },
}
</script>

<style scoped>
    footer {
        margin-top: 63px;
    }

    .links {
        width: 353px;
        margin-top: 60px;
    }

    .footer-socials {
        width: 304px;
        height: 34px;
        margin-top: 29px;
    } 

    .footer-socials-icon {
        width: 34px;
        height: 34px;
    }

    .footer-socials-icon {
        color: #666;
    }

    .footer-socials-icon:hover {
        color: white;
    }

    hr {
       width: 1170px; 
       height: 1px;
       color: #666;
    }

    .rights {
        margin-top: 30px;
        color: #666;
        margin-bottom: 226px;
    }
    .logo-line {
    height: 6px;
    bottom: 12px;
  }
</style>