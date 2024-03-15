<template>
    <h2 v-for="(name) in names" :key="name">{{ name }}</h2>
    <h2 v-for="name in fullNames" :key="name.first">
        {{ name.first }} {{ name.last }}
    </h2>

    <div v-for="dev in devs" :key="dev.name">
        <h2>{{ dev.name }}</h2>
        <h3 v-for="skill in dev.skills" :key="movie">{{ skill }}</h3>
    </div>

    <!-- <h2 v-for="(value, key, index) in myInfo" :key="value">{{ index }} {{ key }} {{ value }}</h2> -->
</template>

<script>
export default {
    name: "ListRendering",
    data() {
        return {
            names: ["Micky", "Nhatty", "Biruk"],
            fullNames: [
                { first: "Mikiyas", last: "Zenebe" },
                { first: "Issac", last: "Seyfu" },
                { first: "Abnet", last: "Melaku" },
            ],
            devs: [
                {
                    name: "DevEd",
                    skills: ["React.JS", "JS Vanilla"],
                },
                {
                    name: "Traversy",
                    skills: ["Backend", "Logic"],
                },
            ],
            myInfo: {
                name: "Mikiyas Zenebe",
                dep: "CS",
                learn: "Vue"
            }
        };
    },
};
</script>
