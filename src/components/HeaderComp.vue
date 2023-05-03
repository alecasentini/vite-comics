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
        <img src="../assets/img/dc-logo.png" alt=" DC Logo">
        <nav>
            <ul>
                <li v-for="(elem, index) in menuLinks" :key="index">
                    <a :class="elem.current ? 'active' : ''" :href="elem.url">{{ elem.nome }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style></style>
