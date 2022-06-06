<template>
    <div class="card">
        <img :src="thumb" :alt="series">
        <h4>{{series}}</h4>
    </div>
</template>

<script>
export default {
    name: 'CommonCard',
    props: {
        thumb: String,
        series: String,
    },
}
</script>

<style lang="scss" scoped>
.card {
    text-align: left;

    img {
        object-fit: contain;
        object-position: top;
        width: 100%;
    }
    h4 {
        margin-top: 0.6rem;
        font-weight: 500;
        font-size: var(--font-sm);
    }
}
</style>