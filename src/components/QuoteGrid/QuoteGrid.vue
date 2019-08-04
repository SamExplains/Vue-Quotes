<template>
    <div class="row">
        <quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">
            <p :id="index">{{ quote.substr(0, 50) + '...' }}</p>
        </quote>
    </div>
</template>

<script>
    import Quote from "../Quote/Quote";
    export default {
        components: {Quote},
        props: {
            quotes: {
                type: Array,
                required: true
            }
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
            }
        }
    };
</script>
