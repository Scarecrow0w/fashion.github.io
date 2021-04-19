<template>
    <header class="flex">
        <div class="absolute w-full header-bg"></div>  
        <div class="flex flex-col justify-between text-white heading ">
            <span class="heading-title">VEHICLE</span>
            <h1 class="font-serif font-bold">One of Saturn's largest rings may be newer than anyone</h1>
            <div class="flex justify-between w-1/2 font-serif heading-info">
                <span>June 6, 2019</span>
                <span><span class="text-gray-200">By </span>Rickie Baroch</span>
                <span>4 comments</span>
            </div>
        </div>
    </header>
</template>

<style scoped>
    header {
        height: calc(100vh - 64px);     
    }

    .header-bg {
        background: url('../src/assets/img/yellowdress.png') no-repeat bottom;
        background-size: cover;
        transform: matrix(-1, 0, 0, 1, 0, 0);
        filter: contrast(65%);    
        z-index: -999;  
        height: calc(100vh - 64px);   
        top: 64px;
    }

    .heading {
        margin-left: 20%;
        width: 560px;
        height: 160px;
        margin-top: 30%;
    }

    .heading-title {
        font-size: 14px;
        line-height: 18.12px;
    }

    .heading h1 {
        font-size: 40px;
        line-height: 50px;
    }

    .heading-info {
        font-size: 14px;
        line-height: 18.55px;
    }
</style>