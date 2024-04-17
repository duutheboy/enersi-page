<template>
    <main>
        <div class="home-container">
            <div class="left">
                <div class="text-top">
                    <h1 id="logo">Ener<span>SI</span></h1>
                </div>
                <div class="text-bot">
                    <p id="logo-snd">Transformando o futuro, <span>um watt de cada vez.</span></p>
                    <a target="_blank" href="https://github.com/duutheboy/enersi-page">
                        <div class="button-container">
                            <p class="button">Junte-se a nós</p>
                        </div>
                    </a>
                </div>
            </div>
            <div class="right">
                <div class="home-img">
                    <img id="img-home" style="width: 450px;" src="https://raw.githubusercontent.com/duutheboy/resources-enersi/master/assets/imgs/home.png" alt="">
                </div>
            </div>
        </div>
    </main>
</template>

<script>
 export default {
    name: "AppHome"
 }
</script>

<style scoped>

    #img-home{
        filter: 
        drop-shadow(10px 0px 260px rgba(9, 255, 0, 0.686))
        brightness(1)
        contrast(120%)
        saturate(150%);
        animation: float 3s ease-in-out infinite;
    }

    h1 {
        font-size: 6rem;
        color: var(--cor-verde-default);
        text-align: center;
        font-weight: bolder;
    }

    .text-bot {
        margin-top: -5%;
    }

    h1 span {
        color: var(--cor-branco-default);
    }

    #logo-snd {
        font-size: 1rem;
        color: var(--cor-branco-default);
        align-items: center;
        font-weight: bold;
    }

    .button-container {
        width: 100%; /* Para garantir que o botão ocupe toda a largura */
        display: flex;
        justify-content: center; /* Centraliza horizontalmente */
        margin-top: 8%;
    }

    .button {
        width: 70%; /* Largura do retângulo */
        height: 5rem; /* Altura do retângulo */
        background-color: var(--cor-verde-default); /* Cor de fundo do retângulo */
        border-radius: 100px; /* Raio da borda para criar cantos arredondados */
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 1.09rem;
        color: white; /* Cor do texto */
        font-weight: bold; /* Peso da fonte */
        cursor: pointer; 
        text-shadow: 2px 2px 0px #55555585;
        transition: 0.6s;
    }

    .button:hover {
        -webkit-box-shadow: 0px 8px 60px -6px var(--cor-verde-default);
        -moz-box-shadow: 0px 8px 60px -6px var(--cor-verde-default);
        box-shadow: 0px 8px 60px -6px var(--cor-verde-default);
    }

    p span {
        color: var(--cor-verde-default);
    }

    .home-container {
        display: grid;
        grid-template-columns: 1fr 1fr; /* Duas colunas com larguras iguais */
        justify-items: center; /* Centraliza os itens horizontalmente */
    }

    .left, .right {
        display: flex;
        flex-direction: column;
        justify-content: center; /* Centraliza os itens verticalmente */
        align-items: center;
        padding: 5%;
    }

    .right {
        padding-right: 20%;
    }

    .left {
        padding-left: 30%;
    }

    #logo {
        text-align: center;
    }

    @keyframes float { 
    0%, 100% {
        transform: 
        rotate(13.69deg)
        translateY(0);
    }
    50% {
        transform: 
        rotate(13.69deg)
        translateY(-5px);
    }}

</style>
