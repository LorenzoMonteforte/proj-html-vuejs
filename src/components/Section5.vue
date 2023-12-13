<script>
export default {
    name: "Section5",
    data() {
        return {
            cards: [
                {
                    img: "img/agreement-business-businessman-872957-1000x580.jpg",
                    title: "Winning your businnes",
                    description: "Never settle for less! You can have everything you want and need. Use the most powerful",
                    date: "February 17, 2019"
                },
                {
                    img: "img/apps-cellphone-communication-340103-1000x580.jpg",
                    title: "Selling Strategies",
                    description: "Never settle for less! You can have everything you want and need. Use the most powerful",
                    date: "February 16, 2019"
                },
                {
                    img: "img/bags-best-friends-daylight-1516440-1000x580.jpg",
                    title: "Good Grades",
                    description: "Never settle for less! You can have everything you want and need. Use the most powerful",
                    date: "February 16, 2019"
                }
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
        <div>
            <h2>Latest Blog Posts</h2>
            <div id="cardContainer">
                <div v-for="card in cards">
                    <img :src="getImagePath(card.img)">
                    <div class="info">
                        <h3>{{ card.title }}</h3>
                        <p class="marTop1rem">{{ card.description }}</p>
                        <div class="marTop2rem">
                            <div class="date">{{ card.date }}</div>
                            <strong>
                                <div class="button">></div>
                            </strong>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="newsletter">
            <div>
                <h2>Subscrive now to our newsletter!</h2>
            </div>
            <div>
                <input type="text" placeholder="Email address...">
                <button> ></button>
            </div>
        </div>
    </section>
</template>

<style scoped>
section>div:first-child {
    padding: 3rem;
}

section>div:first-child>h2 {
    font-size: 3rem;
}

#cardContainer {
    margin-top: 3rem;
    display: flex;
    justify-content: space-between;
}

#cardContainer>div {
    width: 30%;
    border-radius: 0.5rem;
    box-shadow: 1px 1px 5px 1px black;
}

#cardContainer>div>img {
    width: 100%;
    border-top-left-radius: 0.5rem;
    border-top-right-radius: 0.5rem;
}

.info {
    padding: 2rem;
}

.info>p {
    color: grey;
}

.date {
    color: red;
}

.button {
    padding: 1rem 1.1rem;
    border-radius: 50%;
    background-color: rgba(233, 215, 88, 255);
    color: white;
}

.info>div {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

#newsletter {
    background-color: rgb(199, 81, 81);
    margin-top: 3rem;
    padding: 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

#newsletter>div {
    width: 50%;
}

#newsletter h2 {
    font-size: 2rem;
    color: white;
}

#newsletter input {
    height: 4rem;
    border: none;
    border-radius: 2rem;
    padding: 0 1rem;
    width: 80%;
}

#newsletter button {
    color: white;
    background-color: rgba(233, 215, 88, 255);
    padding: 0 2rem;
    border: 0;
    border-radius: 50%;
    translate: -75%;
}

#newsletter>div:last-child {
    display: flex;
    justify-content: flex-end;
}
</style>