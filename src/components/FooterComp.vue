<script>
export default {
    name: "FooterComp"
}
</script>

<template>
    <footer>
        <div id="links">
            <div class="container">
                <div class="col">
                    <h3>dc comics</h3>
                    <ul>
                        <li> <a href="#">Characters</a> </li>
                        <li> <a href="#">Comics</a> </li>
                        <li> <a href="#">Movies</a> </li>
                        <li> <a href="#">TV</a> </li>
                        <li> <a href="#">Games</a> </li>
                        <li> <a href="#">Video</a> </li>
                        <li> <a href="#">News</a> </li>
                    </ul>

                    <h3>shop</h3>
                    <ul>
                        <li> <a href="#">Shop DC</a> </li>
                        <li> <a href="#">Shop DC Collectibles</a> </li>
                    </ul>

                </div>

                <div class="col">
                    <h3>dc</h3>
                    <ul>
                        <li> <a href="#">Terms Of Use</a> </li>
                        <li> <a href="#">Privacy policy (New)</a> </li>
                        <li> <a href="#">Ad Choices</a> </li>
                        <li> <a href="#">Advertising</a> </li>
                        <li> <a href="#">Jobs</a> </li>
                        <li> <a href="#">Subscriptions</a> </li>
                        <li> <a href="#">Talent Workshops</a> </li>
                        <li> <a href="#">CPSC Certificates</a> </li>
                        <li> <a href="#">Ratings</a> </li>
                        <li> <a href="#">Shop Help</a> </li>
                        <li> <a href="#">Contact Us</a> </li>
                    </ul>
                </div>

                <div class="col">
                    <h3>sites</h3>
                    <ul>
                        <li> <a href="#">DC</a> </li>
                        <li> <a href="#">MAD Magazine</a> </li>
                        <li> <a href="#">DC Kids</a> </li>
                        <li> <a href="#">DC Universe</a> </li>
                        <li> <a href="#">DC Power Visa</a> </li>
                    </ul>

                </div>
            </div>
        </div>

        <div id="socials">
            <div class="container">
                <span class="btn">sign-up now!</span>

                <div>
                    <span>follow us</span>
                    <ul>
                        <li><a href="#"><img src="../assets/img/footer-facebook.png" alt="fb"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-twitter.png" alt="tw"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-youtube.png" alt="yt"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt="pn"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-periscope.png" alt="pr"></a></li>
                    </ul>
                </div>
            </div>

        </div>

    </footer>
</template>

<style lang="scss">
footer {
    #links {
        background-image: url(../assets/img/footer-bg.jpg);
        color: white;

        .container {
            width: 80%;
            margin: 0 auto;
            background-image: url(../assets/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-size: 40%;
            background-position: center right;
            display: flex;

            .col {
                padding: 40px 20px;

                h3 {
                    text-transform: uppercase;
                    padding: 20px 0 15px 0;
                }

                ul {
                    li {
                        list-style-type: none;
                        margin-top: 1.5px;
                        margin-bottom: 1.5px;

                        a {
                            text-decoration: none;
                            color: #797979;
                            font-size: 14px;

                            &:hover {
                                color: white;
                            }
                        }
                    }
                }
            }
        }
    }

    #socials {
        width: 100%;
        background-color: #303030;
        padding: 20px 0;

        .container {
            width: 80%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;

            .btn {
                padding: 10px;
                border: 2px solid #0282f9;
                text-transform: uppercase;
                color: white;
                background-color: #303030;
                font-weight: bolder;

                &:hover {
                    background-color: #0282f9;
                    cursor: pointer;
                }
            }

            div {
                display: flex;
                align-items: center;

                span {
                    text-transform: uppercase;
                    color: #0282f9;
                    font-weight: bolder;
                    margin-right: 10px;
                }

                ul {

                    display: flex;

                    li {
                        list-style-type: none;

                        img {
                            margin: 0 10px;

                            &:hover {
                                filter: invert(93%) sepia(94%) saturate(0%) hue-rotate(248deg) brightness(106%) contrast(106%);
                            }

                        }
                    }
                }
            }
        }
    }
}
</style>