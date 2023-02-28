<template>
    <div>
        <HeroComponent />
        <CardContainer />
    </div>
</template>

<script>
import CardContainer from '../components/Card/CardContainer.vue';
import HeroComponent from '../components/Hero/HeroContainer.vue';
    export default {
        name: "ExerciseOnePage",
        components: {
    HeroComponent,
    CardContainer
}
    }
</script>