<script>
import JumbotronComp from './JumbotronComp.vue'
import CurrentSeriesComp from './CurrentSeriesComp.Vue';
export default {
    name: "MainComp",

    components: {
        JumbotronComp,
        CurrentSeriesComp
    },

    data() {
        return {
            menuLinks: [
                {
                    nome: 'digital comics',
                    url: '/digital-comics',
                    image: '/src/assets/img/buy-comics-digital-comics.png'
                },
                {
                    nome: 'dc merchandise',
                    url: '/dc-merchandise',
                    image: '/src/assets/img/buy-comics-merchandise.png'

                },
                {
                    nome: 'subscription',
                    url: '/subscription',
                    image: '/src/assets/img/buy-comics-subscriptions.png'
                },
                {
                    nome: 'comic shop locator',
                    url: '/comic-shop-locator',
                    image: '/src/assets/img/buy-comics-shop-locator.png'
                },
                {
                    nome: 'dc power visa',
                    url: '/dc-power-visa',
                    image: '/src/assets/img/buy-dc-power-visa.svg'
                },
            ]
        }
    }

}
</script>
<template>
    <main>
        <JumbotronComp />
        <div class="top">
            <div id="current-series">
                <span>current series</span>
                <CurrentSeriesComp />
            </div>
            <div id="more">load more</div>
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
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction: column;

        #current-series {
            width: 80%;
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            padding: 40px 0;
            justify-content: space-between;
            position: relative;

            span {
                color: white;
                position: absolute;
                background-color: #0282f9;
                padding: 15px 30px;
                top: -35px;
                text-transform: uppercase;
                font-weight: bold;
                font-size: 25px;
                line-height: 40px;
            }


        }

        #more {
            margin: 20px auto;
            padding: 10px 50px;
            color: white;
            background-color: #0282f9;
            text-transform: uppercase;
            font-weight: bold;

            &:hover {
                cursor: pointer;
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

            ul {
                display: flex;
                height: 100%;
                align-items: center;
                justify-content: space-between;

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

                    img {
                        min-height: 50px;
                        max-height: 70px;
                        min-width: 50px;
                        max-width: 70px;
                    }
                }
            }
        }
    }
}
</style>