<script>
import Navbar from './Navbar.vue';
export default {
    name: "PageHeader",
    components: {
        Navbar
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
            ]
        }
    }
}
</script>

<template>
    <header>
        <div>
            <div>
                <img id="logo" src="../assets/img/theme_eduprime_logo.png" alt="Logo Eduprime">
            </div>
            <div>
                <Navbar :navbarItems="navbarItems" />
            </div>
            <div>
                <button id="btn">
                    <strong>VIEW COURSES</strong>
                </button>
            </div>
        </div>
    </header>
</template>

<style scoped>
header {
    height: 1000px;
    background-color: red;
    padding-top: 3rem;
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

#btn {
    font-size: 1rem;
    padding: 1.5rem 3rem;
    border: none;
    border-radius: 2rem;
    color: white;
    background-color: rgba(233, 215, 88, 255);
}
</style>