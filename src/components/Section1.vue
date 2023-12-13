<script>
import SectionDescriptionImage from './SectionDescriptionImage.vue';
export default {
    name: "Section1",
    components: {
        SectionDescriptionImage
    },
    data() {
        return {
            info: {
                logo: "img/Books-icon.png",
                title: "Thousands of courses for any type of student",
                description: "At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.",
                button: "Browse trough courses",
                image: "img/Graduation-Illustration.png"
            }
        }
    }
}
</script>

<template>
    <section>
        <SectionDescriptionImage :info="info" />
    </section>
</template>

<style scoped>
section {
    background-image: url("../assets/img/home-background.png");
    background-position-x: 100%;
    background-position-y: 50%;
    background-size: 90%;
    background-repeat: no-repeat;
}
</style>