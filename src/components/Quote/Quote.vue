<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="card">
            <div class="card-body">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    .card {
        transition: all ease-in-out .5s;
        &:hover {
            background: rgba(66, 185, 131, 0.51);
        }

    }
</style>

<script>
    export default {
    };
</script>
