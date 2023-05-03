<script>
export default {
    name: "MainComp",
    data() {
        return {
            menuLinks: [
                {
                    nome: 'digital comics',
                    url: '/digital-comics',
                    image: '../assets/img/buy-comics-digital-comics.png'
                },
                {
                    nome: 'dc merchandise',
                    url: '/dc-merchandise',
                    image: '../assets/img/buy-comics-merchandise.png'

                },
                {
                    nome: 'subscription',
                    url: '/subscription',
                    image: '../assets/img/buy-comics-subscription.png'
                },
                {
                    nome: 'comic shop locator',
                    url: '/comic-shop-locator',
                    image: '../assets/img/buy-comics-shop-locator.png'
                },
                {
                    nome: 'dc power visa',
                    url: '/dc-power-visa',
                    image: '../assets/img/buy-dc-power-visa.svg'
                },
            ]
        }
    }

}
</script>
<template>
    <main>
        <div class="top">
            <div>
                <h2>Contents go here</h2>
            </div>
        </div>
        <div class="bottom">
            <div>
                <ul>
                    <li v-for="(elem, index) in menuLinks" :key="index">
                        <img :src="elem.image" :alt="elem.nome">
                        <a :href="elem.url">{{ elem.nome }}</a>
                    </li>
                </ul>

            </div>
        </div>
    </main>
</template>
<style lang="scss">
main {
    .top {
        background-color: #1c1c1c;
        height: 150px;
        width: 100%;
        display: flex;
        justify-content: center;

        div {
            width: 80%;
            display: flex;
            align-items: center;

            h2 {
                color: white;
            }
        }
    }

    .bottom {
        background-color: #0282f9;
        height: 200px;
        width: 100%;
        display: flex;
        justify-content: center;

        div {
            width: 80%;
            display: flex;
            align-items: center;

            ul {
                display: flex;
                height: 100%;
                align-items: center;

                li {
                    list-style-type: none;
                    margin: 0 10px;
                    height: 100%;
                    display: flex;
                    align-items: center;

                    a {
                        text-decoration: none;
                        color: white;
                        padding: 15px;
                        text-transform: uppercase;
                        height: 100%;
                        align-items: center;
                        display: flex;

                    }
                }
            }
        }
    }
}
</style>