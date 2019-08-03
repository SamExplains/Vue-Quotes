<template>
    <div class="row">
        <form action="">
            <div class="col-8">
                <div class="form-group">
                    <label for="">Quote</label>
                    <textarea v-model="quote" class="form-control" name="" id="" rows="3"></textarea>
                </div>
                <div class="form-group">
                    <button class="btn btn-primary" @click.prevent="createNewQuote"></button>
                </div>
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

            }
        }
    };
</script>
