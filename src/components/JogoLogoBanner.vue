<template>
    <div id="logoJogo">

    </div>
</template>

<style scoped>

    div#logoJogo{
        width: 280px;
        height: 154px;
        background: no-repeat center /cover ;
        align-self: start;
        justify-self: center;
    }
    section.diablo div#logoJogo{
        background-image:url(../../public/banner-hero/games/diablo-logo.png) ;
    }

    section.heartStone div#logoJogo{
        background-image:url(../../public/banner-hero/games/hearthstone-logo.png) ;
    }

    section.wow div#logoJogo{
        background-image:url(../../public/banner-hero/games/wow-logo.png) ;
    }

    @media (max-width:792px){
        div#logoJogo{
            position: absolute;
            align-self: start;
            justify-self: end;
            margin-top: -40px;
        }   
    }

    @media (max-width:628px){
        div#logoJogo{
            display: none;
        }
    }
</style>