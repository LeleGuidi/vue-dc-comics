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
    .main {
        background-color: var(--tertiary-color);
        &_container {   
            max-width: var(--container-lg);
            margin: var(--margin-auto);
            h1 {
                color: var(--text-white);
            }
        }
    }
</style>

