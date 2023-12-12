<script>
export default {
    name: "Section1"
}
</script>

<template>
    <section>
        <div>
            <img src="../assets/img/Books-icon.png" alt="Icona libri">
            <h2 class="marTop1rem">Thousands of courses for any type of student</h2>
            <p class="marTop2rem">
                At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you can find a course that
                satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked
                as the most versatile university in the world, thanks to the number of courses it provides.
            </p>
            <button class="marTop2rem">
                <strong>Browse trough courses</strong>
            </button>
        </div>
        <div>
            <img src="../assets/img/Graduation-illustration.png" alt="Cappello da laureato">
        </div>
    </section>
</template>

<style scoped>
section {
    display: flex;
    padding: 3rem;
    background-image: url("../assets/img/home-background.png");
    background-position-x: 100%;
    background-position-y: 50%;
    background-size: 90%;
    background-repeat: no-repeat;
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
    background-color: rgb(231, 200, 92);
}

section>div:last-child>img {
    width: 100%;
}

section>div:last-child {
    display: flex;
    align-items: center;
}
</style>