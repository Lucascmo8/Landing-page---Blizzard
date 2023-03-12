<template>
    <header>
        <img src="../../public/logo-blizzard.png" alt="logo blizzard" id="logo">

        <nav>
            <details>
                <summary>Jogos</summary>
                <div>
                    Oi vamosla
                </div>
            </details>

            <details>
                <summary>
                    Esportes
                </summary>
                
                <div>
                    Oi vamosla
                </div>

            </details>
            <a href="#">Loja</a>
            <a href="#">Notícias</a>
            <a href="#">Suporte</a>
        </nav>

        <div id="botaoHeader">
            <button id="botaoCriarConta">Criar conta</button>
            <button id="botaoLogarConta">Logar</button>
        </div>
        <button id="botaoMenuMobile">
            <img id="imagemMenuMobile" src="../../public/menuMobile.png" alt="">
        </button>
    </header>
    
</template>
im
<script>
    export default{
        name:"HeaderMenu",
        data(){
            return{
                logoSrc:"../../public/logo-blizzard.png",
            }
        }
    }
</script>

<style scoped>
    header{
        display: grid;
        grid-template-columns: 1fr 2fr 1fr;
        padding: 10px 20px 30px;

        border-bottom:1px solid rgba(207, 207, 207, 0.245) ;
    }

    #logo{
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

    #botaoHeader{
        justify-self: center;
        display: flex;
        align-items: center;
        gap:16px
    }

    #botaoHeader>button{
        width: 150px;
        height: 42px;
        padding: 10px 25px;
        font-size: 14px;
        border-radius:4px ;
        transition: background .5s ease-in-out
    }

    #botaoCriarConta{
        border:2px solid #fff;
        background: transparent;
    }

    #botaoLogarConta{
        background: #00AEFF;
    }

    button:hover{
        background: #006c9e;
    }

    #botaoMenuMobile{
        width:30px;
        height: 30px;
        background: transparent;
        border: none;
        align-self: center;
        justify-self: end;
        display: none;
    }

    #imagemMenuMobile{
        width:28px;
        height: 28px;
    }

    @media (max-width:956px){
        header{
            grid-template-columns: 1fr 2fr .2fr;
        }

        nav{
            display: none;
        }

        #botaoMenuMobile{
            display: block;
        }
    }

    @media (max-width:600px){
        header{
            grid-template-columns: 1fr 2fr ;
        }

        #botaoHeader{
            display: none;
        }
    } 
</style>