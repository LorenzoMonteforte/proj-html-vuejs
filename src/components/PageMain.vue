<script>
import Section1 from './Section1.vue';
import Section2 from './Section2.vue';
import Section3 from './Section3.vue';
import Section4 from './Section4.vue';
import Section5 from './Section5.vue';
import Section7 from './Section7.vue';
export default {
    name: "PageMain",
    components: {
        Section1,
        Section2,
        Section3,
        Section4,
        Section5,
        Section7
    }
}
</script>

<template>
    <main>
        <Section1 />
        <Section2 />
        <Section3 />
        <Section4 />
        <Section5 />
        <Section7 />
    </main>
</template>

<style scoped></style>