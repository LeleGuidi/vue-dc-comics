<template>
    <section class="section_hero">
        <img src="../../assets/img/jumbotron.jpg" alt="">
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    .section_hero {
        font-size: 0;
        overflow: hidden;

        img {
            object-fit:cover;
            object-position:top;
            width: 100%;
            height: 300px;
        }
    }
</style>