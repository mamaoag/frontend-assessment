<template>
    <div>
        <article v-if="content" class="tab__content" v-html="content"></article>
    </div>
</template>

<script>
    export default {
        name: "TabContentComponent",
        props: {
            content: String,
        }
    }
</script>
