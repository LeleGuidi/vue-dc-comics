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
    font-size: 0;
    img {
        width: 100%;
        object-fit: cover;
        object-position: top;
        margin-bottom: 0.6rem;
        height: 10.4994rem;
    }
    h4 {
        font-weight: 500;
        font-size: var(--font-sm);
    }
}
</style>