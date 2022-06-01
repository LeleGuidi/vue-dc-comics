<template>
    <header class="header">
        <div class="header_container">
            <div class="header_logo">
                <img src="../assets/img/dc-logo.png" alt="DC LOGO">
            </div>
            <div class="header_nav">
                <nav>
                    <ul>
                        <li v-for="(link, index) in links" :key="index" :class="{active : link.current == true}">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'BaseHeader',
    data() {
        return {
            links: [
            {
                text: 'Characters',
                url: '#/',
                current: false,
            },
            {
                text: 'Comics',
                url: '#/',
                current: true,
            },
            {
                text: 'Movies',
                url: '#/',
                current: false,
            },
            {
                text: 'TV',
                url: '#/',
                current: false,
            },
            {
                text: 'Games',
                url: '#/',
                current: false,
            },
            {
                text: 'Collectibles',
                url: '#/',
                current: false,
            },
            {
                text: 'Video',
                url: '#/',
                current: false,
            },
            {
                text: 'Fans',
                url: '#/',
                current: false,
            },
            {
                text: 'News',
                url: '#/',
                current: false,
            },
            {
                text: 'Shop',
                url: '#/',
                current: false,
            }
            ]
        }  
    }
}
</script>

<style scoped lang="scss">
@import '../assets/style/mixins.scss';
.header {
    padding: 0.5rem;
    text-transform: uppercase;
    &_container {
        max-width: var(--container-lg);
        @include flex ('between', 'center');
        margin: var(--margin-auto);
    }
    &_logo {
        img {
            width: 80px;
        }
    }
    &_nav{
        ul {
            @include listInLine;
            a {
                text-decoration: none;
                padding: 0 0.8rem;
                font-size: var(--font-sm);
                font-weight: 500;
                color: var(--secondary-color);
                
            }
            .active a {
                border-bottom: 2px solid var(--primary-color);
            }
        }
    }
}
    
</style>