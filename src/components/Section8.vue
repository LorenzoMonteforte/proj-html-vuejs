<script>
export default {
    name: "Section8",
    data() {
        return {
            persone: [
                {
                    icon: "img/Fac-Comp-Science.png",
                    description: "“I can’t thank EduPrime enough for what it has done for me. I am now a successful doctor at one of the best clinics in the world.”",
                    foto: "img/testimonial-2-student-1.png",
                    name: "Mask Stevens",
                    professione: "Student (2012 - 2016)"
                },
                {
                    icon: "img/Fac-Medicine.png",
                    description: "“The most beautiful experience a student can have is attending EduPrime – the best university in the world. I strongly encourage everyone to apply.”",
                    foto: "img/testimonial-1-student-1.png",
                    name: "Andrew Jackson",
                    professione: "Student(2015-2018)"
                },
                {
                    icon: "img/Fac-Comp-Science.png",
                    description: "“I can’t thank EduPrime enough for what it has done for me. I am now a successful doctor at one of the best clinics in the world.”",
                    foto: "img/testimonial-2-student-1.png",
                    name: "Eduard Lopez",
                    professione: "Student (2010 - 2014)"
                },
                {
                    icon: "img/Fac-Medicine.png",
                    description: "“The most beautiful experience a student can have is attending EduPrime – the best university in the world. I strongly encourage everyone to apply.”",
                    foto: "img/testimonial-1-student-1.png",
                    name: "Will Smith",
                    professione: "Student (2005- 2009)"
                },
            ],
            indice: [0, 1]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        },
        avanti: function () {
            for (let i = 0; i < 2; i++) {
                if (this.indice[i] >= (this.persone.length - 2)) {
                    if (i == 0) {
                        this.indice[i] = 0;
                    }
                    if (i == 1) {
                        this.indice[i] = 1;
                    }
                } else {
                    this.indice[i] = this.indice[i] + 2;
                }
            }
        }
    }
}
</script>

<template>
    <section>
        <h2>Thoughts from our students</h2>
        <div id="cardContainer">
            <div v-for="n in 2">
                <img class="logo" :src="getImagePath(this.persone[this.indice[(n - 1)]].icon)">
                <p>{{ persone[indice[(n - 1)]].description }}</p>
                <div class="infoContainer">
                    <div class="imgContainer">
                        <img :src="getImagePath(this.persone[this.indice[(n - 1)]].foto)">
                    </div>
                    <div>
                        <h3>{{ persone[indice[(n - 1)]].name }}</h3>
                        <p>{{ persone[indice[(n - 1)]].professione }}</p>
                    </div>
                </div>
            </div>
        </div>
        <div>
            <button>indietro</button>
            <button @click="avanti()">avanti</button>
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

#cardContainer {
    width: 100%;
    margin-top: 3rem;
    display: flex;
    justify-content: space-between;
}

#cardContainer>div {
    width: 48%;
    border-radius: 1rem;
    padding: 4rem 3rem;
    box-shadow: 1px 1px 10px 1px gray;
}

.logo {
    height: 3rem;
}

.infoContainer {
    width: 100%;
    display: flex;
    align-items: center;
    margin-top: 3rem;
}

.imgContainer {
    width: 15%;
    aspect-ratio: 1;
    background-color: pink;
    border-radius: 50%;
    overflow: hidden;
}

.infoContainer>div:last-child {
    padding-left: 1rem;
}

.imgContainer>img {
    width: 100%;
    display: block;
}

#cardContainer>div>p {
    margin-top: 3rem;
}
</style>