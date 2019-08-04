<template>
    <div class="row">
        <form class="col-8 mx-auto" action="">
            <div class="form-group">
                <label for="">Create New Quote</label>
                <textarea v-model="quote" class="form-control" name="" id="" rows="3"></textarea>
            </div>
            <div class="form-group">
                <button class="btn btn-primary" @click.prevent="createNewQuote">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        props: {
        },
        data() {
            return {
                quote: null,
            }
        },
        methods: {
            createNewQuote() {
                this.$emit('quoteAdded', this.quote);
                this.quote = null;
            }
        }
    };
</script>
