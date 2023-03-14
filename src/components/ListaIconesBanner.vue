<template>
    <ul>
        <li>
            <input type="radio" id="diablo" value="diablo" name="diablo" v-model="jogoEscolhido" @change="mostrarImagemBanner('diablo')">
            <label for="diablo"><img ref="opcao" class="none" data-jogos="diablo" src="../../public/banner-hero/icons/game-1.png" alt=""></label>
        </li>

        <li>
            <input type="radio" id="heartStone" value="heartStone" v-model="jogoEscolhido" @change="mostrarImagemBanner('heartStone')">
            <label for="heartStone"><img ref="opcao" class="none" data-jogos="heartStone"  src="../../public/banner-hero/icons/game-2.png" alt=""></label>
        </li>

        <li>
            <input type="radio" id="wow" value="wow" v-model="jogoEscolhido" @change="mostrarImagemBanner('wow')">
            <label for="wow"><img ref="opcao" class="none"  data-jogos="wow" src="../../public/banner-hero/icons/game-3.png" alt=""></label>
        </li>

        <li><img class="none" src="../../public/banner-hero/icons/game-4.png" alt=""></li>
        <li><img class="none" src="../../public/banner-hero/icons/game-5.png" alt=""></li>
    </ul>
</template>

<script>
    export default{
        name:"ListaIconesBanner",
        data(){
            return{
                jogoEscolhido:"diablo"
            }
        },
        methods:{
            mostrarImagemBanner(event){
                console.log(event)
                this.jogoEscolhido = event;
                this.$emit("jogo-escolhido", this.jogoEscolhido)
            }
        },
        mounted(){
            console.log(this.$refs.opcao)
        }
    }
</script>

<style scoped>
    ul{
        width: 50px;
        list-style: none;
        justify-self: center;
        align-self: center;
        grid-row: 1/3;
        grid-column:1;

        display: flex;
        flex-direction: column;
        gap: 20px;
    }   
        
    input{
        display: none;
    }

    img,li,label{
        width:48px;
        height: 48px;
    }

    input:checked + label>img{
        filter: grayscale(0);
    }

    img.none{
        filter: grayscale(1);
    }

    @media (max-width:792px){
        ul{
            width: 89vw;
            grid-row: 2/3;
            justify-self: start;
            flex-direction: row;
            flex-wrap: wrap;
        }
    }

    @media (max-width:550px){
        ul{
            justify-self: start;
            align-self: center;
        }
    }
</style>