<script >
export default {
    name: "HeaderComp",
    data() {
        return {
            menuLinks: [
                {
                    nome: 'characters',
                    url: '/characters',
                    current: false
                },
                {
                    nome: 'Comics',
                    url: '/comics',
                    current: true
                },
                {
                    nome: 'movies',
                    url: '/movies',
                    current: false
                },
                {
                    nome: 'tv',
                    url: '/tv',
                    current: false
                },
                {
                    nome: 'games',
                    url: '/games',
                    current: false
                },
                {
                    nome: 'collectibles',
                    url: '/collectibles',
                    current: false
                },
                {
                    nome: 'videos',
                    url: '/videos',
                    current: false
                },
                {
                    nome: 'fans',
                    url: '/fans',
                    current: false
                },
                {
                    nome: 'news',
                    url: '/news',
                    current: false
                },
                {
                    nome: 'shop',
                    url: '/shop',
                    current: false
                }
            ]
        }
    }
}
</script>

<template>
    <header>

        <nav>
            <img src="../assets/img/dc-logo.png" alt=" DC Logo">
            <ul>
                <li v-for="(elem, index) in menuLinks" :key="index">
                    <a :class="elem.current ? 'active' : ''" :href="elem.url">{{ elem.nome }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
header {
    display: flex;
    height: 150px;
    width: 100%;
    background-color: white;
    justify-content: center;

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 80%;

        ul {
            display: flex;
            align-items: center;

            li {
                list-style-type: none;
                margin: 0 10px;
                line-height: 145px;
                display: flex;
                align-items: center;

                a {
                    text-decoration: none;
                    color: black;
                    text-transform: uppercase;
                    font-weight: bolder;
                    align-items: center;
                    display: flex;

                    &:hover {
                        border-bottom: 5px solid #0282f9;
                        color: #0282f9;
                    }

                }


            }
        }
    }
}

.active {
    border-bottom: 5px solid #0282f9;
    color: #0282f9;

}
</style>
