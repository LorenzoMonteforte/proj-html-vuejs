<script>
import Navbar from './Navbar.vue';
import Carousel from './Carousel.vue';
export default {
    name: "PageHeader",
    components: {
        Navbar,
        Carousel
    },
    data() {
        return {
            navbarItems: [
                {
                    title: "Home",
                    arrow: true
                },
                {
                    title: "Courses",
                    arrow: true
                },
                {
                    title: "About Us",
                    arrow: false
                },
                {
                    title: "News",
                    arrow: true
                },
                {
                    title: "Pages",
                    arrow: true
                },
                {
                    title: "Contact",
                    arrow: false
                },
                {
                    title: "Purchase",
                    arrow: false
                }
            ],
            infoCarousel: [
                {
                    title: "Showcase your courses",
                    description: "EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.",
                    background: "red"
                },
                {
                    title: "Key to your success",
                    description: "EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.",
                    background: "yellow"
                },
                {
                    title: "Lead. Inspire. Win!",
                    description: "EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.",
                    background: "green"
                }
            ]
        }
    },
    methods: {
        changeBackground: function (indexCarousel) {
            let header = document.getElementById("header");
            header.style.backgroundColor = this.infoCarousel[indexCarousel].background;
        }
    }
}
</script>

<template>
    <header id="header">
        <div>
            <div>
                <img id="logo" src="../assets/img/theme_eduprime_logo.png" alt="Logo Eduprime">
            </div>
            <div>
                <Navbar :navbarItems="navbarItems" />
            </div>
            <div>
                <button class="btn btnYellow">
                    <strong>VIEW COURSES</strong>
                </button>
            </div>
        </div>
        <div>
            <Carousel :infoCarousel="infoCarousel" @invokeChangeBackground="changeBackground" />
        </div>
        <img src="../assets/img/Wave-1.png" alt="Immagine onda">
    </header>
</template>

<style scoped>
header {
    background-color: red;
    padding-top: 3rem;
    overflow: hidden;
}

header>div:first-child {
    display: flex;
    padding: 0 3rem;
}

header>div:first-child>div:first-child,
header>div:first-child>div:last-child {
    width: 25%;
}

header>div:first-child>div:nth-child(2) {
    width: 50%;
    display: flex;
    align-items: center;
    padding: 0 1.5rem;
}

#logo {
    width: 100%;
}

header>div:first-child>div:first-child {
    padding-right: 1.5rem;
    display: flex;
    align-items: center;
}

header>div:first-child>div:last-child {
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

header>div:nth-child(2) {
    margin-top: 6rem;
}

header>img {
    margin-top: 6rem;
    width: 100vw;
    scale: 1.5;
}
</style>