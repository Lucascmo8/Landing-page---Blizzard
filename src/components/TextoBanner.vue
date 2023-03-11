<template>
    <div id="texto">
        <h1>
            Retorne à escuridão com o game Diablo IV
        </h1>
        <p>
            O retorno de Lilith traz uma era de escuridão e sofrimento
        </p>
        <button>
            Jogue agora
        </button>
    </div>
</template>

<script>
    export default{
        name:"TextoBanner",
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

        width: 168px;
        height: 52px;

        background: #00AEFF;
        border-radius: 4px;
        transition: background .5s ease-in-out
    }

    button:hover{
        background: #006c9e;
    }
</style>