<template>
    <main class="main">
        <div class="main_container">
            <h1> Content goes here </h1>
        </div>
    </main>
</template>

<script>
export default {
    
}
</script>

<style scoped lang="scss">
@import '../assets/style/mixins.scss';
    .main {
        background-color: var(--tertiary-color);
        &_container {   
            max-width: var(--container-lg);
            margin: var(--margin-auto);
            height: 8rem;
            @include flex('start', 'center');
            h1 {
                color: var(--text-white);
            }
        }
    }
</style>

