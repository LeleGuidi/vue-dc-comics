<template>
    <main class="main">
        <SectionHero/>
        <SectionCards/>
    </main>
</template>

<script>
import SectionHero from '../sections/SectionHero.vue'
import SectionCards from '../sections/SectionCards.vue'
export default {
    name: 'BaseMain',
    components: { 
        SectionHero, 
        SectionCards 
    },
    
}
</script>

<style scoped lang="scss">
@import '../../assets/style/mixins.scss';
.main {
    background-color: #1c1c1c;
}
</style>

