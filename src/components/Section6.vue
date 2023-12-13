<script>
export default {
    name: "Section6",
    data() {
        return {
            persone: [
                {
                    img: "img/member-mentors-5-500x500.jpg",
                    name: "Bruno Dias",
                    qualifica: "Assistan Manager"
                },
                {
                    img: "img/member-mentors-2-500x500.jpg",
                    name: "Laura Zola",
                    qualifica: "Assistan Manager"
                },
                {
                    img: "img/member-mentors-3-500x500.jpg",
                    name: "Thomas Moriz",
                    qualifica: "Regional Manager"
                },
                {
                    img: "img/member-mentors-4-500x500.jpg",
                    name: "Emma Ava",
                    qualifica: "General Director"
                },
                {
                    img: "img/member-mentors-1-500x500.jpg",
                    name: "Sophia Doe",
                    qualifica: "Assistan Manager"
                },
            ],
            indici: [0, 1, 2, 3]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        },
        avanti: function () {
            for (let i = 0; i < 4; i++) {
                if (this.indici[i] == (this.persone.length - 1)) {
                    this.indici[i] = 0;
                } else {
                    this.indici[i]++;
                }
            }
        },
        indietro: function () {
            for (let i = 0; i < 4; i++) {
                if (this.indici[i] == 0) {
                    this.indici[i] = (this.persone.length - 1);
                } else {
                    this.indici[i]--;
                }
            }
        }
    }
}
</script>

<template>
    <section>
        <h2>Management</h2>
        <p class="marTop2rem">A team of expert teachers that are leading our university! Meet our staff and become a student
            at EduPrime this
            year!</p>
        <div id="cardsContainer" class="marTop2rem">
            <div>
                <button @click="indietro()" class="button">
                    <font-awesome-icon icon="fa-solid fa-chevron-left" />
                </button>
            </div>
            <div>
                <div class="card" v-for="n in 4">
                    <div>
                        <img :src="getImagePath(this.persone[this.indici[(n - 1)]].img)">
                    </div>
                    <h3 class="marTop1rem">{{ persone[indici[(n - 1)]].name }}</h3>
                    <p class="marTop1rem">{{ persone[indici[(n - 1)]].qualifica }}</p>
                </div>
            </div>
            <div>
                <button @click="avanti()" class="button">
                    <font-awesome-icon icon="fa-solid fa-chevron-right" />
                </button>
            </div>
        </div>
        <button class="marTop2rem btn btnYellow">
            <strong>View All Team</strong>
        </button>
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

section>p {
    width: 50%;
    text-align: center;
}

#cardsContainer {
    width: 100%;
    display: flex;
}

#cardsContainer>div:first-child,
#cardsContainer>div:last-child {
    width: 10%;
    position: relative;
}

#cardsContainer>div:nth-child(2) {
    width: 80%;
    display: flex;
}

.card {
    height: 100%;
    width: 25%;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.card>div {
    width: 100%;
    aspect-ratio: 1;
    border-radius: 50%;
    overflow: hidden;
}

.card img {
    width: 100%;
    display: block;
}

.button {
    height: 1rem;
    width: 1rem;
    padding: 1.5rem;
    border: none;
    border-radius: 50%;
    color: white;
    background-color: rgb(199, 81, 81);
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 50%;
    translate: 0 -50%;
}

#cardsContainer>div:first-child>button {
    left: 0;
}

#cardsContainer>div:last-child>button {
    right: 0;
}
</style>