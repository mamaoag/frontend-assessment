<template>
    <div :class="{'active': selected}" class="accordion__content_container">
        <!-- Header -->
        <div class="accordion__header py-2 px-4" @click="handleSelected(accordionItem)">
            <h3>{{ title }}</h3>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="svg_icon">
                <path v-if="!selected" stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                <path v-else stroke-linecap="round" stroke-linejoin="round" d="M19.5 12h-15" />
            </svg>

        </div>
        <!-- Body -->
        <article v-if="selected" class="accordion__content py-2 px-4" v-html="content"></article>
    </div>
</template>

<script>
    export default {
        name: 'AccordionItemComponent.vue',
        props: {
            title: {
                type: String
            },
            content: {
                type: String
            },
            selected: {
                type: Boolean
            },
            accordionItem: {
                type: Number
            }
        },
        methods: {
            handleSelected(idx) {
                this.$emit('handleSelect', idx)
            }
        }
    }
</script>

<style>
.accordion__content_container {
    background: #fff;
}

.svg_icon {
    width: 2rem;
    height: 2rem;
}

.accordion__header {
    display: flex;
    justify-items: center;
    justify-content: space-between;
    align-items: center;
    align-self: center;
}

.accordion__header:hover {
    cursor: pointer;
}

.accordion__header h3 {
    font-weight: bold;
    letter-spacing: 0.06rem;
}

.accordion__content {
    transform: all cubic-bezier(0, 1, 0.5, 1) 0.5s;
}

.accordion__content_container.active {
    background: #fea706;
}
</style>