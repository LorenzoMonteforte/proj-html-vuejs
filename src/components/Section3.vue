<script>
export default {
    name: "Section3",
    data() {
        return {
            tappe1: [
                {
                    title: "Demo Classes",
                    description: "In the first week, students try to accomodate with the teaching style and choose their optional courses"
                },
                {
                    title: "Graduation Day",
                    description: "In the first week, students try to accomodate with the teaching style and choose their optional courses"
                }
            ],
            tappe2: [
                {
                    title: "Orientation",
                    description: "In the first week, students try to accomodate with the teaching style and choose their optional courses"
                },
                {
                    title: "Evaluation",
                    description: "In the first week, students try to accomodate with the teaching style and choose their optional courses"
                }
            ],
            cards: [
                {
                    title: "Coaching Session",
                    data: "20 May 21:30 PM",
                    description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Pariatur, officia non eaque eveniet laborum soluta."
                },
                {
                    title: "Coaching Session",
                    data: "24 Mar 18:00 PM",
                    description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Pariatur, officia non eaque eveniet laborum soluta."
                },
                {
                    title: "Coaching Session",
                    data: "12 Feb 13:30 PM",
                    description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Pariatur, officia non eaque eveniet laborum soluta."
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <h2>University Year</h2>
        <div id="container">
            <div id="firstContainer">
                <div class="container" v-for="tappa in tappe1">
                    <div>
                        <h4>{{ tappa.title }}</h4>
                        <p class="marTop1rem">{{ tappa.description }}</p>
                    </div>
                </div>
            </div>
            <img src="../assets/img/Timeline-Item.png" alt="">
            <div id="secondContainer">
                <div class="container" v-for="tappa in tappe2">
                    <div>
                        <h4>{{ tappa.title }}</h4>
                        <p class="marTop1rem">{{ tappa.description }}</p>
                    </div>
                </div>
            </div>
        </div>
        <img src="../assets/img/upcoming-events-calendar-icon.png" alt="">
        <h2 class="marTop1rem">Upcoming Events</h2>
        <div id="cardContainer" class="marTop2rem">
            <div v-for="card in cards">
                <h4>{{ card.title }}</h4>
                <div class="marTop0_5rem">{{ card.data }}</div>
                <p class="marTop0_5rem">{{ card.description }}</p>
                <button>Find More</button>
            </div>
        </div>
        <button id="allEvent">
            <strong>View All Event</strong>
        </button>
    </section>
</template>

<style scoped>
section {
    background-color: rgb(199, 81, 81);
    padding: 4rem 5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
}

section>h2 {
    font-size: 3rem;
    color: white;
}

#container {
    width: 100%;
    margin-top: 6rem;
}

#container>img {
    width: 100%;
}

#firstContainer {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    color: white;
}

.container {
    height: 100%;
    width: 40%;
    padding: 1rem 1rem;
}

.container>div {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.container p {
    text-align: center;
}

#secondContainer {
    width: 100%;
    display: flex;
    justify-content: flex-start;
    color: white;
}

section>img {
    margin-top: 3rem;
    width: 8%;
}

#cardContainer {
    width: 100%;
    display: flex;
    justify-content: space-between;
}

#cardContainer>div {
    width: 30%;
    background-color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    padding-bottom: 3rem;
    border-radius: 1rem;
    position: relative;
}

#cardContainer button {
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

#cardContainer p {
    text-align: center;
}

#allEvent {
    font-size: 1rem;
    margin-top: 6rem;
    padding: 1.5rem 3rem;
    color: white;
    background-color: rgb(231, 200, 92);
    border: none;
    border-radius: 2rem;
}
</style>