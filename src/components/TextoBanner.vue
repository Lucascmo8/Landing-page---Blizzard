<template>
    <div id="texto">
        <h1>
            {{ titulo }}
        </h1>
        <p>
            {{ texto }}
        </p>
        <button>
            Jogue agora
        </button>
    </div>
</template>

<script>
    export default{
        name:"TextoBanner",
        props:{
            jogo:{
                type:String,
                required:true
            }
        }
        ,
        data() {
            return {
                titulo: 'Retorne à escuridão com o game Diablo IV',
                texto: 'O retorno de Lilith traz uma era de escuridão e sofrimento'
            }
        },
        watch:{
            jogo: function(){
                this.mudarTextos()
            }
        },
        methods:{
            mudarTextos(){
                if(this.jogo == "diablo"){
                    this.titulo= 'Retorne à escuridão com o game Diablo IV'
                    this.texto= 'O retorno de Lilith traz uma era de escuridão e sofrimento'
                }else if(this.jogo == "wow"){
                    this.titulo= 'Desbrave as Terras Sombrias em Shadowlands! '
                    this.texto= 'O que jaz além do mundo que você conhece?'
                }else{
                    this.titulo= 'Novo pacote de expansão de Hearthstone'
                    this.texto= 'A Horda e a Aliança se encontraram no Vale Alterac para lutar'
                }
            }
        },
        mounted(){
            this.mudarTextos()
        }
    }
</script>

<style scoped>
    #texto{
        max-width: 562px;
        min-width: 283px;
        display: flex;
        flex-direction: column;
        grid-row: 1/3;
        grid-column:2;
        box-sizing: border-box;
    }

    h1{
        max-width: 562px;
        min-width: 283px;
        margin-bottom: 16px;
        font-size: 64px;
        font-weight: 700;
    }

    p,button{
        font-size: 18px;
    }

    button{
        padding: 14px 32px;
        margin-top: 32px;

        width: 178px;
        height: 52px;

        background: #00AEFF;
        border-radius: 4px;
        transition: background .5s ease-in-out
    }

    button:hover{
        background: #006c9e;
    }

    @media (max-width:792px){
        #texto{
            max-width: 545px;
            min-width: 283px;
            display: flex;
            flex-direction: column;
            grid-row: 1/2;
            grid-column:1/3;
            z-index: 3;
        }
    }

    @media (max-width:580px){
        #texto{
            width: 283px;
        }

        h1{
            font-size: 44px;
            width: 283px;
        }

        p{
            max-width:283px;
            font-size: 16px;
        }
    }
</style>