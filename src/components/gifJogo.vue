<template>
    <div id="gifContainer">
        <p>Assista o trailer</p>
        <div id="gifJogos">

        </div >
    </div>
</template>



<style scoped>

    div#gifContainer{
        width: 280px;
        height: 178px;

        grid-row: 2;
        grid-column: 3;
        align-self: center;
        justify-self: center;

        text-align: end;
        font-size: 13px;
        font-weight: 600;
    }

    #gifJogos{
        margin-top:16px ;
        width: 280px;
        height: 158px;
        background-size: cover;
        background-position: center bottom;
        background-repeat: no-repeat;
    }

    section.diablo #gifJogos{
        background-image:url(../../public/banner-hero/games/diablo-animation-cover.png) ;
    }

    section.diablo #gifJogos:hover , section.diablo #gifJogos:focus{
        background-image:url(../../public/banner-hero/games/diablo-animation.gif);
    }

    section.heartStone #gifJogos{
        background-image:url(../../public/banner-hero/games/hearthstone-animation-cover.png) ;
    }

    section.heartStone #gifJogos:hover , section.diablo #gifJogos:focus{
        background-image:url(../../public/banner-hero/games/hearthstone-animation.gif);
    }

    section.wow #gifJogos{
        background-image:url(../../public/banner-hero/games/wow-animation-cover.png) ;
    }

    section.wow #gifJogos:hover , section.diablo #gifJogos:focus{
        background-image:url(../../public/banner-hero/games/wow-animation.gif);
        background-size: 310px 215px;
        background-position: center;
        object-position: 100px;
    }

    @media (max-width:792px){
        div#gifContainer{
            position: absolute;
            align-self: end;
            justify-self: end;
            margin-bottom: 40px;
        }   
    }

    @media (max-width:675px){
        div#gifContainer{
            display: none;
        }
    }
</style>