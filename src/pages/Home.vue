<template>
    <main>
        <div class="home-container">
            <div class="left">
                <div class="text-top">
                    <h1 id="logo">Ener<span>SI</span></h1>
                </div>
                <div class="text-bot">
                    <p id="logo">Transformando o futuro, <span>um watt de cada vez.</span></p>
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
        brightness(0.86)
        contrast(170%)
        saturate(200%);
        animation: float 2s ease-in-out infinite;
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

    p {
        font-size: 1.1rem;
        color: var(--cor-branco-default);
        align-items: center;
        font-weight: bold;
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