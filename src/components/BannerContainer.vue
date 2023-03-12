<template>
    <section class="diablo">
        <HeaderMenu :logo="logoSrc"/>
        <div id="itensBanner">
            <ListaIconesBanner />
            <TextoBanner />
            <JogoLogoBanner />
            <gifJogo />
        </div>
    </section>
</template>

<script>
    import HeaderMenu from './HeaderMenu.vue';
    import TextoBanner from './TextoBanner.vue';
    import ListaIconesBanner from './ListaIconesBanner.vue';
    import JogoLogoBanner from './JogoLogoBanner.vue';
    import gifJogo from './gifJogo.vue';
    export default{
        name:"BannerContainer",
        components:{
            HeaderMenu,
            TextoBanner,
            ListaIconesBanner,
            JogoLogoBanner,
            gifJogo,
        },
        
    }
</script>

<style scoped>
    section{
        height: 736px;
        width:100%;
        background: no-repeat 40% center /cover ;
        box-sizing: border-box;
    }
    section.diablo{
        background-image:url(../../public/banner-hero/games/diablo-bg.png) ;
    }

    section.heartStone{
        background-image:url(../../public/banner-hero/games/hearthstone-bg.png) ;
    }

    section.wow{
        background-image:url(../../public/banner-hero/games/wow-bg.png) ;
    }

    div#itensBanner{
        display: grid;
        padding: 0 35px;
    }

    @media (min-width:792px){
        div#itensBanner{
            margin-top:111px;
            grid-template-columns: 1fr 2fr 1fr;
            grid-template-rows:1fr 1fr;
            align-items: start;
        }
    }

    @media (max-width:792px){
        div#itensBanner{
            margin-top:90px;

            grid-template-columns:2fr .5fr;
            grid-template-rows:2fr 1fr;
            align-items: start;
        }
    }

    @media (max-width:475px){
        div#itensBanner{
            grid-template-columns:1fr;
            grid-template-rows:2fr 1fr;
            align-items: start;
        }
    }
</style>