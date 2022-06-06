<template>
    <div class="card">
        <div class="card_img">
            <img :src="thumb" :alt="series">
        </div>
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

    &_img {
        width: 100%;
        height: 0;
        padding-bottom: 100%;
        overflow: hidden;
        margin-bottom: 0.6rem;

        img {
        width: 100%;
        object-fit: cover;
        object-position: top;
        }
    }
    
    h4 {
        font-weight: 500;
        font-size: var(--font-sm);
    }
}
</style>