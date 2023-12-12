<script>
export default {
    name: "Navbar",
    props: {
        navbarItems: Array
    }
}
</script>

<template>
    <nav>
        <ul>
            <li v-for="navbarItem in navbarItems">
                <strong>
                    {{ navbarItem.title }}
                    <font-awesome-icon class="marLef0_5rem" icon="fa-solid fa-caret-down" v-if="navbarItem.arrow == true" />
                </strong>
            </li>
        </ul>
    </nav>
</template>

<style scoped>
ul {
    list-style-type: none;
}

nav>ul>li:first-of-type {
    color: rgba(233, 215, 88, 255);
}

nav>ul {
    display: flex;
    justify-content: space-between;
}

nav {
    width: 100%;
}

nav>ul>li {
    color: white;
}
</style>