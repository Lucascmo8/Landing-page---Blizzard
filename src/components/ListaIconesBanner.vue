<template>
    <ul>
        <li><img src="../../public/banner-hero/icons/game-1.png" alt=""></li>
        <li><img src="../../public/banner-hero/icons/game-2.png" alt=""></li>
        <li><img src="../../public/banner-hero/icons/game-3.png" alt=""></li>
        <li><img class="none" src="../../public/banner-hero/icons/game-4.png" alt=""></li>
        <li><img class="none" src="../../public/banner-hero/icons/game-5.png" alt=""></li>
    </ul>
</template>

<style>
    ul{
        width: 50px;
        list-style: none;
        justify-self: center;
        align-self: center;
        grid-row: 1/3;
        grid-column:1;

        display: flex;
        flex-direction: column;
        gap: 20px;
    }   
        

    img,li{
        width:48px;
        height: 48px;
    }

    img.none{
        filter: grayscale(1);
    }

    @media (max-width:792px){
        ul{
            width: 89vw;
            grid-row: 2/3;
            justify-self: start;
            flex-direction: row;
            flex-wrap: wrap;
        }
    }

    @media (max-width:550px){
        ul{
            justify-self: start;
            align-self: center;
        }
    }
</style>