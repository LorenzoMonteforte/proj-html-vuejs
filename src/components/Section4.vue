<script>
import SectionDescriptionImage from './SectionDescriptionImage.vue';
import SectionImageDescription from './SectionImageDescription.vue';
export default {
    name: "Section4",
    components: {
        SectionDescriptionImage,
        SectionImageDescription
    },
    data() {
        return {
            courses: [
                {
                    logo: "img/Decisions-icon.png",
                    title: "Make Better Decision",
                    teacher: "James Colins",
                    price: "$21.00"
                },
                {
                    logo: "img/Speaker-icon.png",
                    title: "How to be a speacker",
                    teacher: "James Colins",
                    price: "Free"
                },
                {
                    logo: "img/Network-icon.png",
                    title: "Network Introductions",
                    teacher: "James Colins",
                    price: "Free"
                },
                {
                    logo: "img/Brand-icon.png",
                    title: "Brand Management",
                    teacher: "James Colins",
                    price: "Free"
                },
            ],
            info: {
                logo: "img/Exam-icon.png",
                title: "The most efficient examination method",
                description: "EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.",
                button: "Discover the Method",
                image: "img/Exam-Illustration.png"
            },
            info2: {
                logo: "img/Exam-icon-1.png",
                title: "Variable fees for international students",
                description: "EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.",
                button: "List of Fees",
                image: "img/Girl-Illustration.png"
            }
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
        <h2>Latest Courses</h2>
        <div id="cardContainer">
            <div v-for="course in courses">
                <img :src="getImagePath(course.logo)">
                <h4 class="marTop2rem">{{ course.title }}</h4>
                <div class="marTop1rem">Teacher :
                    <strong>{{ course.teacher }}</strong>
                </div>
                <div class="marTop1rem">Price :
                    <strong>{{ course.price }}</strong>
                </div>
                <button id="viewCourse">
                    <strong>View Course</strong>
                </button>
            </div>
        </div>
        <SectionDescriptionImage :info="info" />
        <SectionImageDescription :info="info2" />
    </section>
</template>

<style scoped>
section {
    padding: 3rem;
}

section>h2 {
    font-size: 3rem;
}

#cardContainer {
    margin-top: 3rem;
    display: flex;
    justify-content: space-between;
}

#cardContainer>div {
    width: 22.5%;
    border-radius: 3px;
    padding: 2rem;
    padding-bottom: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    background-color: white;
    box-shadow: 1px 1px 5px 1px black;
}

#cardContainer>div>img {
    width: 50%;
}

#viewCourse {
    padding: 1rem 2rem;
    border: none;
    border-radius: 2rem;
    position: absolute;
    bottom: 0;
    translate: 0 50%;
    color: white;
    background-color: rgb(199, 81, 81);
    box-shadow: 1px 1px 5px 1px black;
}
</style>