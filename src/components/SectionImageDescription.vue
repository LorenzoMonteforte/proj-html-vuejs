<script>
export default {
    name: "SectionImageDescription",
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
            <img v-if="info.logo != ''" :src="getImagePath(info.logo)">
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
    background-position-x: 100%;
    background-position-y: 50%;
    background-size: 90%;
    background-repeat: no-repeat;
    width: 100%;
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
    background-color: rgb(199, 81, 81);
}

section>div:last-child>img {
    width: 75%;
}

section>div:last-child {
    display: flex;
    align-items: center;
    justify-content: center;
}

section>div:first-child {
    order: 2;
}

section>div:last-child {
    order: 1;
}
</style>