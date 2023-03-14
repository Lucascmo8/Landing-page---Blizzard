<template>
    <div>
        
    </div>
</template>

<script>
    export default{
        name:"ImagemBattleNet",
    }
</script>

<style scoped>
    div{
        position: relative;
        
        width: 100%;
        display: flex;
        background-image: url(../../public/ilustrations/app.png), url(../../public/ilustrations/app-mini.png);
        background-position: 20% 70%, 50% 110%;
        background-size: 1053.33px 593.96px, 562.86px 346.19px;
        background-repeat: no-repeat, no-repeat;
        background-blend-mode: saturation;
    }

    @media (max-width:820px){
        div{
            height: 300px;
            background-position: 100% 70%, 100% 110%;
            background-size: 528px 300px, 280px 170px;
        }
    }
    
</style>