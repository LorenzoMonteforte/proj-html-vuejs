<script>
export default {
    name: "PageFooter",
    data() {
        return {
            getEduprime: [
                "Request a website",
                "Browse Themes",
                "Payment options",
                "Support System",
                "Checkout",
                "Purchase Theme"
            ],
            networking: [
                "Purchase Theme",
                "Our Benefits",
                "Our Team",
                "Our Services",
                "Other Products",
                "My account"
            ],
            categorie: [
                "ECONOMY",
                "DESIGN",
                "COACHING",
                "BUSINNES",
                "MEDICINE",
                "LAW",
                "FITNESS"
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div id="first">
            <img src="../assets/img/theme_eduprime_logo.png" alt="">
            <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses,
                secondary schools etc.</p>
            <div>
                <div class="socialContainer">a</div>
                <div class="socialContainer">a</div>
                <div class="socialContainer">a</div>
            </div>
        </div>
        <div>
            <h3>Get Eduprime</h3>
            <ul>
                <li v-for="items in getEduprime">{{ items }}</li>
            </ul>
        </div>
        <div>
            <h3>Networking</h3>
            <ul>
                <li v-for="items in networking">{{ items }}</li>
            </ul>
        </div>
        <div id="fourth">
            <div>
                <input type="text" placeholder="Search">
                <button> ></button>
            </div>
            <h3>Search categories</h3>
            <div class="etichette">
                <div v-for="categoria in categorie">{{ categoria }}</div>
            </div>
            <div id="diritti">ModelTheme. All rights reserved.</div>
        </div>
    </footer>
</template>

<style scoped>
footer {
    height: 500px;
    background-color: rgb(199, 81, 81);
    display: flex;
    padding: 5rem 3rem;
    color: white;
}

footer>div:nth-child(1),
footer>div:nth-child(4) {
    height: 100%;
    width: 30%;
    padding: 1rem;
}

footer>div:nth-child(2),
footer>div:nth-child(3) {
    height: 100%;
    width: 20%;
    padding: 1rem;
}

#first>img {
    width: 80%;
}

#first>p {
    margin-top: 2rem;

}

.socialContainer {
    height: 1rem;
    width: 1rem;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1.5rem;
    border: 2px solid rgba(233, 215, 88, 255);
    background-color: transparent;
}

#first>div {
    margin-top: 2rem;
    display: flex;
    gap: 1rem;
}

ul {
    list-style-type: none;
    margin-top: 2rem;
}

li {
    margin-top: 1rem;
}

li:first-of-type {
    margin-top: 0;
}

#fourth input {
    height: 4rem;
    border: none;
    border-radius: 2rem;
    padding: 0 1rem;
    width: 80%;
}

#fourth button {
    color: white;
    background-color: rgba(233, 215, 88, 255);
    padding: 0 2rem;
    border: 0;
    border-radius: 50%;
    translate: -75%;
}

#fourth>div:first-child {
    display: flex;
    justify-content: flex-end;
}

#fourth h3 {
    margin-top: 2rem;
}

.etichette>div {
    padding: 0.5rem 1rem;
    border: 2px solid white;
    border-radius: 2rem;
    font-size: 0.7rem;
}

.etichette {
    display: flex;
    margin-top: 2rem;
    gap: 0.5rem;
    flex-wrap: wrap;
    justify-content: flex-end;
}

#diritti {
    margin-top: 1rem;
    text-align: end;
    color: rgba(233, 215, 88, 255);
}
</style>