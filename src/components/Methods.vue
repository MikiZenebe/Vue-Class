<template>
    <h3>{{ 2 + 3 + 5 }}</h3>
    <h3>{{ 25 + 10 + 5 }}</h3>

    <h3>Add Method {{ add(2, 5, 5) }}</h3>
    <h3>Multiplier {{ multiply(baseMultiplier) }}</h3>
</template>

<script>
export default {
    name: "Methods",
    data() {
        return {
            baseMultiplier: 5
        };
    },
    methods: {
        add(a, b, c) {
            return a + b + c
        },
        multiply(num) {
            return num * this.baseMultiplier
        }
    }
};
</script>
