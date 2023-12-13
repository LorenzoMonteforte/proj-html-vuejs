<script>
export default {
    name: "Section1",
    props: {
        info: Object
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
        <div>
            <img :src="getImagePath(info.logo)">
            <h2 class="marTop1rem">{{ info.title }}</h2>
            <p class="marTop2rem">{{ info.description }}</p>
            <button class="marTop2rem">
                <strong>{{ info.button }}</strong>
            </button>
        </div>
        <div>
            <img :src="getImagePath(info.image)">
        </div>
    </section>
</template>

<style scoped>
section {
    display: flex;
    padding: 3rem;
}

section>div {
    width: 50%;
    padding: 3rem;
}

section>div:first-child>img {
    width: 10%;
}

section>div:first-child>h2 {
    font-size: 3rem;
}

section>div:first-child>button {
    padding: 1.5rem 3rem;
    border: none;
    border-radius: 2rem;
    color: white;
    background-color: rgb(231, 200, 92);
}

section>div:last-child>img {
    width: 100%;
}

section>div:last-child {
    display: flex;
    align-items: center;
}
</style>