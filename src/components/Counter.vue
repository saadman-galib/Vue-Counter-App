<template>
    <div class="counter-app-container">
        <h1 class="counter-heading">Counter</h1>
        <p id="counter">{{ count }}</p>
        <div class="button-container">
            <button
                id="decrease"
                aria-label="decrease button"
                @click="decreaseCount"
            >
                {{ decrease }}
            </button>
            <button
                id="increase"
                aria-label="increase button"
                @click="increaseCount"
            >
                {{ increase }}
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Vue Counter App",
    data() {
        return {
            count: 0,
            increase: "Increase Count",
            decrease: "Decrease Count",
        };
    },
    methods: {
        increaseCount() {
            this.count++;
        },
        decreaseCount() {
            if (this.count <= 0) {
                this.count = 0;
            } else {
                this.count--;
            }
        },
    },
};
</script>
