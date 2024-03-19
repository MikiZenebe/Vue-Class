<template>
    <h2>{{ name }}</h2>
    <div>
        <button v-on:click="changeName">Click Change name</button>
        <button v-on:mouseover="name = 'Is Good'">Hover to Change name</button>
    </div>

    <h2>{{ count }}</h2>
    <div>
        <button @click="Increment(5)">Increment 5</button>
        <button @click="Decrement(10)">Decrement 10</button>
    </div>
</template>

<script>
export default {
    name: "EventHandler",
    data() {
        return {
            name: "Event Handler",
            count: 0,
        };
    },

    methods: {
        changeName(event) {
            this.name = "Micky"
            console.log("Event", event)
        },
        Increment(num) {
            this.count += num
        },
        Decrement(num) {
            this.count -= num
        }
    },
};
</script>
