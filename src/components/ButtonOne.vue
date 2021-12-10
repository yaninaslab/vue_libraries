<template>
    <div>
<button @click="get_quote">Get Quote</button>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        name: "button-one",
        methods: {
            get_quote() {
                axios.request({
                    url: "http://philosophy-quotes-api.glitch.me/quotes"

                }).then((response) => {
                    //var quote = response.data['quote'];
                    this.$emit('button_clicked', response.data);
                }).catch((error) => {
                    error;
                    this.$emit('button_clicked', "Issue with API, sorry");
                });
            }
        },
    }
</script>

<style scoped>

</style>