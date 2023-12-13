<script>
import SectionImageDescription from "./SectionImageDescription.vue"
export default {
    name: "Section2",
    components: {
        SectionImageDescription
    },
    data() {
        return {
            facultiesList: [
                {
                    logo: "img/Gavel-v2.png",
                    title: "Law Faculty",
                    image: "img/Gavel-Illustration-e1556884768193.png",
                    description: "Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions."
                },
                {
                    logo: "img/Coins-tabs-v2.png",
                    title: "Economy",
                    image: "img/Economy.png",
                    description: "Economics focuses on the behaviour and interactions of economic agents and how economies work. Microeconomics analyzes basic elements in the economy, including individual agents and markets, their interactions, and the outcomes of interactions, including unemployment of resource."
                },
                {
                    logo: "img/Medicine-tabs-v2.png",
                    title: "Medicine",
                    image: "img/Medicine.png",
                    description: "Medicine is the science and practice of establishing the diagnosis, prognosis, treatment, and prevention of disease. Medicine encompasses a variety of health care practices evolved to maintain and restore health by the prevention and treatment of illness."
                },
                {
                    logo: "img/Computer-tabs-v2.png",
                    title: "Computer Science",
                    image: "img/Computer-Science.png",
                    description: "Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation software systems."
                },
                {
                    logo: "img/Palette-tabs-v2.png",
                    title: "Graphic Design",
                    image: "img/Graphic-Design.png",
                    description: "Graphic design is the process of visual communication and problem-solving through the use of typography, photography and illustration. The field is considered a subset of visual communication and communication design, but sometimes the term ``graphic design`` is used synonymously."
                },
            ],
            info: {
                logo: "",
                title: "Law Faculty",
                description: "Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.",
                image: "img/Gavel-Illustration-e1556884768193.png",
                button: "Read More",
                logo2: "img/Gavel-v2.png"
            }
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        },
        createProps: function (i) {
            this.info.title = this.facultiesList[i].title;
            this.info.description = this.facultiesList[i].description;
            this.info.image = this.facultiesList[i].image;
            this.info.logo2 = this.facultiesList[i].logo
            let array = document.getElementsByClassName("cardContainer");
            let array2 = document.getElementsByClassName("logo");
            let array3 = document.getElementsByClassName("title");
            for (let index = 0; index < this.facultiesList.length; index++) {
                array[index].style.backgroundColor = "white";
                array2[index].style.filter = "";
                array3[index].style.color = "rgb(217, 104, 102)";
            }
            array[i].style.backgroundColor = "rgb(217, 104, 102)";
            array2[i].style.filter = "brightness(0) invert(1)";
            array3[i].style.color = "white";
        }
    }
}
</script>

<template>
    <section id="section">
        <h2>Faculties available at EduPrime</h2>
        <p class="marTop2rem">A single university with a load of courses, tailored to satisfy any student’s needs.</p>
        <div class="marTop2rem">
            <div class="cardContainer" v-for="(facultie, i) in facultiesList" @click="createProps(i)">
                <img class="logo" :src="getImagePath(facultie.logo)">
                <h4 class="marTop1rem title">{{ facultie.title }}</h4>
            </div>
        </div>
        <SectionImageDescription :info="info" />
    </section>
</template>

<style scoped>
#section {
    padding-top: 4rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

section>h2 {
    font-size: 3rem;
}

section>p {
    text-align: center;
    width: 30%;
}

section>div {
    width: 100%;
    padding: 0 4rem;
    display: flex;
}

section>div>div {
    height: 100%;
    width: calc(100% / 5);
    border: 1px solid black;
    padding: 2rem 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.cardContainer>img {
    width: 100%;
}

.cardContainer>h4 {
    color: rgb(199, 81, 81);
}
</style>