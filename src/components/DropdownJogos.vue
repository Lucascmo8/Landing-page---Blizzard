<template>
    <button @click.prevent="toogleJogos()" class="btnHeader">Jogos</button>
    <div v-if="estaAberto">
        <ul>
            <li v-for="(jogo,index) in jogosLogo" :key="index">
                <img :src="jogo.logo" :alt="jogo.name">
                <p>{{ jogo.name }}</p>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:"DropdownJogos",
        data() {
            return {
                jogosLogo:[],
                estaAberto:false,
            }
        },
        methods: {
            async mostrarLogoJogos() {
                const req = await fetch('https://api.brchallenges.com/api/blizzard/games')
                const data = await req.json()
                this.jogosLogo = data
            },
            toogleJogos(){
                this.estaAberto = !this.estaAberto
                this.mostrarLogoJogos()
            }
        },
        mounted(){
            this.mostrarLogoJogos()
        }
    }
</script>

<style scoped>
    div{
        position: absolute;
        top:90.8px;
        left:0 ;
        background-color: #212428;
        z-index: 1;
        height: calc(736px - 90.8px);
        width: 100%;

        display: flex;
        align-items: center;
        transition: .5s ease-in-out;
    }

    ul{
        width: 100%;
        display: grid;
        grid-template-columns: repeat(4,1fr);
        justify-items: center;
        z-index: 3;
        gap:30px;
        text-align: center;
        font-weight: 700;
    }

    li{
        display: flex;
        flex-direction: column;
        align-content: center;
        justify-content: center;
        z-index: 3;
        width: 110px;
        gap:16px;
    }

    li>img{
        width: 100px;
        height: 80px;
        z-index: 3;
        justify-self: center;
        align-self: center;
    }
</style>