<template>
    <header>
        <img :src="logo" alt="">

        <nav>
            <details>
                <summary>Jogos</summary>
                <div>
                    Oi vamosla
                </div>
            </details>

            <details>
                <summary>Esportes</summary>
                <div>
                    Oi vamosla
                </div>
            </details>
            <a href="#">Loja</a>
            <a href="#">Notícias</a>
            <a href="#">Suporte</a>
        </nav>

        <div id="buttonHeader">
            <button>Criar conta</button>
            <button>Logar</button>
        </div>
    </header>
    
</template>
im
<script>
    export default{
        name:"HeaderMenu",
        props:['logo'],
        
    }
</script>

<style scoped>
    header{
        display: grid;
        grid-template-columns: 1fr 2fr 1fr;
        padding: 10px 20px 30px;

        border-bottom:1px solid rgba(207, 207, 207, 0.245) ;
    }

    img{
        width:100px;
        height: 50px;
        justify-self: center;
        border-bottom:1px solid rgb(8, 127, 231) ;
    }
    
    nav{
        display: flex;
        align-items: center;
        font-size: 14px;
        color:#fff;
        gap:34px;
    }

    #buttonHeader{
        justify-self: center;
        display: flex;
        align-items: center;
    }
</style>