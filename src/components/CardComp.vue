<script>

export default {
    name: "CardComp",

    props: {
        img: String,
        price: String,
        series: String,
        type: String

    }
}
</script>

<template>
    <div class="flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img src="img" alt="">
            </div>
            <div class="flip-card-back">
                <p>{{ series }}</p>
                <p>{{ type }}</p>
                <p>{{ price }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.flip-card {
    background-color: transparent;
    aspect-ratio: 1;
}

.flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    transition: transform 0.8s;
    transform-style: preserve-3d;
}

.gira {
    transform: rotateY(180deg);
}

.flip-card-front,
.flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
}

.flip-card-front img {
    width: 100%;
    height: 100%;
}


.flip-card-back {
    transform: rotateY(180deg);
}
</style>