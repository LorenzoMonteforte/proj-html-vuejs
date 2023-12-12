<script>
export default {
    name: "Carousel",
    props: {
        infoCarousel: Array
    },
    data() {
        return {
            indexCarousel: 0
        }
    },
    methods: {
        avanti: function () {
            if (this.indexCarousel == (this.infoCarousel.length - 1)) {
                this.indexCarousel = 0;
            } else {
                this.indexCarousel++;
            }
        },
        indietro: function () {
            if (this.indexCarousel == 0) {
                this.indexCarousel = (this.infoCarousel.length - 1);
            } else {
                this.indexCarousel--;
            }
        }
    }
}
</script>

<template>
    <div id="carousel">
        <div>
            <button class="btnAvaInd" @click="indietro(), $emit('invokeChangeBackground', this.indexCarousel)">
                <font-awesome-icon icon="fa-solid fa-chevron-left" />
            </button>
        </div>
        <div>
            <h1>{{ infoCarousel[indexCarousel].title }}</h1>
            <p>{{ infoCarousel[indexCarousel].description }}</p>
            <div>
                <button class="btn btnYellow">
                    <strong>
                        <font-awesome-icon class="marRig0_5rem" icon="fa-solid fa-magnifying-glass" />
                        Search courses
                    </strong>
                </button>
                <button class="btn btnWhite">
                    <strong>
                        <font-awesome-icon class="marRig0_5rem" icon="fa-solid fa-user-plus" />
                        Apply for university
                    </strong>
                </button>
            </div>
        </div>
        <div>
            <button class="btnAvaInd" @click="avanti(), $emit('invokeChangeBackground', this.indexCarousel)">
                <font-awesome-icon icon="fa-solid fa-chevron-right" />
            </button>
        </div>
    </div>
</template>

<style scoped>
#carousel {
    width: 100%;
    display: flex;
}

#carousel>div:first-child,
#carousel>div:last-child {
    width: 25%;
    position: relative;
}

#carousel>div:nth-child(2) {
    width: 50%;
    padding: 1rem 0;
}

#carousel>div:first-child>button {
    left: 2rem;
}

h1 {
    text-align: center;
    font-size: 3rem;
    color: white;
}

#carousel>div:nth-child(2)>p {
    margin-top: 3rem;
    text-align: center;
    font-size: 1.25rem;
    color: white;
}

#carousel>div:nth-child(2)>div {
    margin-top: 3rem;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.btnWhite {
    color: rgba(219, 108, 108, 255);
    background-color: white;
}

#carousel>div:last-child>button {
    right: 2rem;
}

.btnAvaInd {
    position: absolute;
    top: 50%;
    translate: 0 -50%;
    font-size: 2.5rem;
    border: none;
    color: white;
    background-color: transparent;
}
</style>