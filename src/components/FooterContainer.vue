<template>
    <footer>
        <div id="textoFooter">
            <img src="../../public/logo-battle-net.png" alt="logo battle net" id="logoBattleNet">
            <h4>Baixe agora o battle.net</h4>
            <ul>
                <li><img src="../../public/Group.svg" alt="">  Seus jogos em um só lugar</li>
                <li><img src="../../public/Group1.svg" alt="">  Conecte-se aos seus amigos</li>
                <li><img src="../../public/buyLogo.png" alt="">  Compre jogos e itens digitais</li>
            </ul>
            <button>
                Baixar para o {{ dispositivoDoUsuario }}
            </button>
            <div id="textoAplicativo">
                <img src="../../public/celular.svg" alt=""> 
                <p>
                    Também disponível como<br> <a>aplicativo móvel</a>
                </p>
            </div>
        </div>
        <ImagensBattleNet />
    </footer>
</template>

<script>
    import ImagensBattleNet from './ImagensBattleNet.vue';
    export default{
        name:"FooterContainer",
        data(){
            return{
                dispositivoDoUsuario:"Windows"
            }
        },
        components:{
            ImagensBattleNet,
        },
        methods:{
            veificarDispositivos(){
                const dispositivo = navigator.userAgent || navigator.vendor || window.opera
                if( dispositivo.match( /iPad/i ) || dispositivo.match( /iPhone/i ) || dispositivo.match( /iPod/i ) || dispositivo.match( "Mac" ) ){
                        this.dispositivoDoUsuario = "MacOS"
                }else if(dispositivo.match( "Linux" )){
                    this.dispositivoDoUsuario = "Linux"
                    
                }else{
                    this.this.dispositivoDoUsuario = "Windowns"
                }
            }
        }
        ,
        mounted(){
           this.veificarDispositivos()
        }
    }
</script>

<style scoped>
    footer{
        background: url(../../public/footer-background.png);
        height: auto;
        width: 100%;
        display: flex;
        justify-content: space-between;
        padding: 100px;
    }

    #textoFooter{
        display: flex;
        flex-direction: column;
        gap: 30px;
        padding: 25px;
    }

    img#logoBattleNet{
        height: 18px;
        width: 130px;
    }

    h4{
        font-size: 28px;
        font-weight: 700; 
    }

    ul{
        display: flex;
        flex-direction: column;
        gap: 24px;
        width: 100%;
    }

    li{
        width: 100%;
        color: #BCC0CA;
        font-size: 18px;
    }

    li>img{
        width: 18px;
        height: 18px;
    }

    button{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 14px 32px;
        gap: 8px;

        width: 266px;
        height: 52px;

        background: #00AEFF;
        border-radius: 4px;

        font-weight: 600;
        font-size: 16px;
    }

    #textoAplicativo{
        display: flex;
        align-items: center;
        gap: 20px;
    }

    #textoAplicativo img{
        width: 20px;
        height: 32px;
    }

    #textoAplicativo p{
        font-weight: 600;
        font-size: 14px;
        line-height: 21px;

        color: #E5E5E5;
    }

    #textoAplicativo a{
        color: #E5E5E5;
        text-decoration: underline;
    }

    @media (max-width:820px){
        footer{
            flex-direction: column;
            padding:48px;
        }
    }
</style>