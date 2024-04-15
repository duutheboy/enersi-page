<template>
    <header>
        <nav class="container">
            <div class="header-content">
                <h1 id="logo"><a href="">Ener<span>SI</span></a></h1>
                <img v-on:click="openMenu" id="menu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" alt="Abrir menu">
            </div>
        </nav>

        <div class="menu-overlay" v-if="menuActive" v-on:click="closeMenu"></div>

        <div id="menu-items" :class="{active:menuActive}">
            <h1 id="menu-logo"><a href="">Ener<span>SI</span></a></h1>
            <ul>
                <li>
                    <a href="/">Home</a>
                </li>
                <li>
                    <a href="/projetos">Projetos</a>
                </li>
                <li>
                    <a href="/contato">Contato</a>
                </li>
                <li>
                    <a href="/sobre">Sobre</a>
                </li>
            </ul>
        </div>
    </header>
</template>


<script>
export default {
    name: 'AppHeader',
    data(){
        return {
            menuActive: false
        }
    },
    methods:{
        openMenu: function() {
            this.menuActive = true;
        },
        closeMenu: function() {
            this.menuActive = false;
        }
    }
}
</script>


<style scoped>
    header {
        background-color: rgba(29, 29, 29, 0);
        width: 100%;
        height: 52px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .header-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    }

    h1 {
        padding: 30px;
        font-size: 1.7rem;
    }

    h1 a {
        color: var(--cor-verde-default);
    }

    h1 span {
        color: var(--cor-branco-default);
    }

    #menu {
        width: 18px;
        cursor: pointer;
        transition: 0.2s opacity;
    }

    #menu:hover {
        opacity: 0.7;
    }

    .menu-overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 60%;
        height: 100vh;
        background-color: black;
        opacity: 0.7;
    }

    #menu-logo {
        font-size: 1.9rem;
        margin-top: 40px;
        text-shadow: 0px 0px 5px rgba(0, 255, 51, 0.6);
    }

    #menu-items {
        position: fixed;
        top: 0;
        right: 0;
        background-color: rgb(32, 32, 32);
        width: 40%;
        height: 100vh;
        display: none;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
    }

    #menu-items.active {
        display: flex;
    }

    ul {
        list-style: none;
        text-align: center;
    }

    ul li {
        margin: 30px 0px;
    }

    ul li a {
        color: var(--cor-branco-default);
        transition: color 0.4s;
        font-weight: bold;
        font-size: 1rem;
    }

    ul li a:hover {
        color: var(--cor-verde-default);
    }

    @media (min-width: 700px) {
        #menu,
        #menu-logo,
        #menu-overlay {
            display: none;
        }

        #menu-items {
            display: flex;
            background-color: rgba(32, 32, 32, 0);
            position: static;
            height: 52px;
            width: auto;
            align-items: center;
            justify-content: center;
        }

        ul {
            display: flex;
            margin-right: 40px;
        }

        ul li {
            margin: 0;
            padding: 30px;
            padding-left: 20px;
            margin-right: 10px;
        }
    }

</style>