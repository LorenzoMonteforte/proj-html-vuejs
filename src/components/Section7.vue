<script>
export default {
    name: "Section7",
    data() {
        return {
            loghi: [
                "img/partner-2.png",
                "img/partner-3.png",
                "img/partner-4.png",
                "img/partner-5.png",
                "img/partner-6.png",
                "img/partner-1.png",
                "img/partner-7.png",
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section>
        <h2>Parthners</h2>
        <div id="subtitle" class="marTop2rem">
            Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to
            corporate strategy.
        </div>
        <div id="parthnerContainer" class="marTop2rem">
            <img v-for="logo in loghi" :src="getImagePath(logo)">
        </div>
    </section>
</template>

<style scoped>
section {
    padding: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

section>h2 {
    font-size: 3rem;
}

#subtitle {
    width: 50%;
    text-align: center;
}

#parthnerContainer {
    width: 100%;
    height: 50px;
    display: flex;
    justify-content: space-between;
}

#parthnerContainer img {
    height: 100%;
}
</style>