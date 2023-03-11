<template>
    <div>
        <p>Assista o trailer</p>
        <img id="teste" src="../../public/banner-hero/games/diablo-animation.gif" alt="" srcset="">
    </div>
</template>

<style scoped>

    div{
        width: 280px;
        height: 178px;

        grid-row:2;
        grid-column: 3;
        align-self: center;
        justify-self: center;

        text-align: end;
        font-size: 13px;
        font-weight: 600;
    }

    img#teste{
        margin-top:16px ;
        width: 280px;
        height: 158px;
    }

    @media (max-width:792px){
        div{
            position: absolute;
            align-self: end;
            justify-self: end;
            margin-bottom: 40px;
        }   
    }

    @media (max-width:675px){
        div{
            display: none;
        }
    }
</style>