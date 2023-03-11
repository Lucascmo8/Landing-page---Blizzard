<template>
    <section class="diablo">
        <HeaderMenu :logo="logoSrc"/>
        <div id="itensBanner">
            <ListaIconesBanner />
            <TextoBanner />
            <JogoLogoBanner />
            <img id="teste" src="../../public/banner-hero/games/diablo-animation.gif" alt="" srcset="">
        </div>
    </section>
</template>

<script>
    import HeaderMenu from './HeaderMenu.vue';
    import TextoBanner from './TextoBanner.vue';
    import ListaIconesBanner from './ListaIconesBanner.vue';
    import JogoLogoBanner from './JogoLogoBanner.vue';
    export default{
        name:"BannerContainer",
        components:{
            HeaderMenu,
            TextoBanner,
            ListaIconesBanner,
            JogoLogoBanner,
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

    div#itensBanner{
        margin-top:111px;

        display: grid;
        grid-template-columns: .5fr 2fr 1fr;
        grid-template-rows:1fr 1fr;
        align-items: start;
    }
    img#teste{
        width: 280px;
        height: 158px;
        grid-row:2;
        grid-column: 3;
        align-self: center;
        justify-self: center;
    }
</style>