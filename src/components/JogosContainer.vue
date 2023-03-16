<template>
    <section>
        <div id="headerJogos">
            <h2>
                Jogos <br> exclusivos
            </h2>

            <ul id="listaDePlataformas">
                <li><img src="../../public/battlenet.svg" alt=""></li>
                <li><img src="../../public/switch.svg" alt=""></li>
                <li><img src="../../public/xbox.svg" alt=""></li>
                <li><img src="../../public/playstation.svg" alt=""></li>
            </ul>
            
            <p>
                Ver todos os Jogos
            </p>
        </div>
        <div id="todosOsJogos">
            <div class="cardDoJogo" v-for="(jogo,index) in jogos" :key="index">
                <img :src="jogo.image" :alt="jogo.name" class="imagemCard">
                <img :src="jogo.logo" :alt="jogo.name" class="logoCard">
                <h3>
                    {{ jogo.name }}
                </h3>
                <p>{{ jogo.category }}</p>
            </div>
            <div class="cardBlizzard">
                <img src="../../public/logo-blizzard.png" alt="logo" id="logoBlizzard">
                <p><img src="../../public/maisjogos.svg"> Ver todos os jogos</p>
            </div>
        </div>
    </section>
</template>

<script>
    export default{
        name:"JogosContainer",
        data() {
            return {
                jogos:[]
            }
        },
        methods: {
            async pegarJogos() {
                const req = await fetch('https://api.brchallenges.com/api/blizzard/games')
                const data = await req.json()
                this.jogos = data
                console.table(data)
            }
        },
        mounted(){
            this.pegarJogos()
        }
    }
</script>

<style scoped>
    section{
        background: #020203;
        padding: 110px;
    }

    div#headerJogos{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 25px;
    }

    div#headerJogos h2{
        font-size: 28px;
        word-wrap: break-word;

    }

    div#headerJogos p{
        font-size: 14px;
        max-width: 120px;
        text-align: end;
    }

    ul#listaDePlataformas{
        display: flex;
        flex-direction: row;
        gap: 24px;
        list-style: none;
    }

    ul#listaDePlataformas img,ul#listaDePlataformas li{
        width: 20px;
        height: 20px;
    }

    #todosOsJogos{
        display:grid;
        justify-items: center;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        gap:32px;
    }

    div.cardDoJogo{
        height: auto;
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr .4fr .1fr;
    }

    div.cardBlizzard,div.cardDoJogo{
            width: 280px;
    }

    div.cardBlizzard{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap:16px;
        min-height: 210px;
        border: 1px solid #212428;
    }

    div.cardBlizzard > img{
        width: 90px;
    }

    div.cardBlizzard > p{
        vertical-align: bottom;
    }
    div.cardBlizzard > p>img{
        width: 14px;
        height: 14px;
        vertical-align: middle;
    }
    img.imagemCard{
        height: 385px;
        width: 280px;
        grid-row:1/3;
        transition: 1s linear;
    }

    img.logoCard{
        width: 150px;
        height: 100px;
        margin-bottom: -150px;

        position: absolute;
        align-self: center;
        justify-self: center;
        grid-row:2;
        
        transition: 1s linear;
    }

    div.cardDoJogo h3{
        font-size:18px;
        align-self: center;
    }

    div.cardDoJogo p{
        font-size:14px ;
    }

    div.cardDoJogo:hover>.imagemCard{
        transform: scale(1.05);
        box-shadow: 0px 0px 4px #fff;
    }



    @media (max-width:1460px){
        section{
            padding:50px;
        }

        #todosOsJogos{
            grid-template-columns: 1fr 1fr 1fr;
            gap:28px;
        }
        
        div.cardBlizzard,div.cardDoJogo{
            width: 200px;
        }

        div.cardDoJogo h3{
            font-size:16px;
        }

        img.imagemCard{
            height: 280px;
            width: 200px;
        }

        div.cardDoJogo:hover>.imagemCard{
            transform: scale(1.04);
        }
        img.logoCard{
            width: 108px;
            height: 70px;
            margin-bottom: -110px;
        }

    }

    @media (max-width:720px){
        section{
            padding:25px;
        }

        #todosOsJogos{
            grid-template-columns: 1fr 1fr;
            gap:16px;
        }

        ul#listaDePlataformas{
            display: none;
        }

        div.cardDoJogo{
            grid-template-columns: 1fr;
            grid-template-rows: 1fr 1fr;
        }

        div.cardBlizzard,div.cardDoJogo{
            width: 160px;
        }

        div.cardBlizzard > img{
            width: 70px;
        }

        div.cardBlizzard > p >img{
            display: none;
        }

        div.cardBlizzard > p{
            font-size: 14px;
        }

        div.cardDoJogo h3, div.cardDoJogo p{
            display: none;
        }

        img.imagemCard{
            height: 210px;
            width: 160px;
        }

        img.logoCard{
            width: 80px;
            height: 55px;
            position: absolute;
            align-self: end;
            justify-self: center;
            grid-row:2;
            margin-bottom:16px;
        }
    }

    @media (max-width:430px){
        section,#headerJogos{
            padding:10px;
        }
        #todosOsJogos{
            grid-template-columns: 1fr;
            gap:24px;
        }

        div.cardBlizzard,div.cardDoJogo{
            width: 200px;
        }

        img.imagemCard{
            height: 280px;
            width: 200px;
        }

        img.logoCard{
            width: 108px;
            height: 70px;
        }
    }
</style>