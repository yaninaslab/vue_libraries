<template>
    <div class="quote_container">
        <p>{{ quote.quote }}</p>
        <h4>{{ quote.source }}</h4>
        <h6>{{ quote.philosophy }}</h6>

    </div>
</template>

<script>
    export default {
        name: "page-quote",
        props: {
           quote: Object

        },
    }
</script>

<style scoped>

</style>