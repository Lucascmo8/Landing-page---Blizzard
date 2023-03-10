<template>
    <section class="diablo">
        <HeaderMenu :logo="logoSrc"/>
        <ListaIconesBanner />
        <TextoBanner />
    </section>
</template>

<script>
    import HeaderMenu from './HeaderMenu.vue';
    import TextoBanner from './TextoBanner.vue';
    import ListaIconesBanner from './ListaIconesBanner.vue';
    export default{
        name:"BannerContainer",
        components:{
            HeaderMenu,
            TextoBanner,
            ListaIconesBanner,
        },
        data(){
            return{
                logoSrc:"../../public/logo-blizzard.png",
            }
        }
    }
</script>

<style scoped>
    section{
        height: 736px;
        width:100%;
        background: no-repeat center /cover ;
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
</style>