<template>
    <div>
        <div class="exercise_2__layout">
            <div class="container">
                <TabContainer :data="data" />
                <AccordionContainer :data="data" />
            </div>
        </div>
    </div>
</template>

<script>
    import AccordionContainer from '../components/Accordion/AccordionContainer.vue';
import TabContainer from '../components/Tab/TabContainer.vue';
import data from '../data/data.json'

    export default {
    name: "ExceriseTwoPage",
    asyncData({ params }) {
        return { data };
    },
    methods: {
        isMobile() {
            return (screen.width <= 760)
        }
    },
    components: { TabContainer, AccordionContainer }
}
</script>

<style>
    .exercise_2__layout {
        display: flex;
        justify-content: center;
        flex-direction: column;
        height: 100vh;
        width: 100vw;
        margin: 0;
        align-items: center;
        background-color: #f2f5f8;
    }
</style>