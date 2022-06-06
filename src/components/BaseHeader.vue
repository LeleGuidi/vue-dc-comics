<template>
    <header class="header">
        <div class="header_container">
            <div class="header_logo">
                <img src="../assets/img/dc-logo.png" alt="DC LOGO">
            </div>
            <div class="header_nav">
                <nav>
                    <ul>
                        <li v-for="(link, index) in links" :key="index" :class="(link.current == true)? 'active' : ''" @click="linkActive(index)">
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
    },
    methods: {
        linkActive(index) {
            if (this.links[index].current == false) {
                !this.links[index].current
            }
        }
    }
}
</script>

<style scoped lang="scss">
@import '../assets/style/mixins.scss';
.header {
    text-transform: uppercase;
    &_container {
        max-width: var(--container-lg);
        @include flex ('between', 'center');
        margin: var(--margin-auto);
    }
    &_logo {
        margin: 0.8rem 0;
        img {
            width: 80px;
            vertical-align: middle
        }
    }
    &_nav{
        ul {
            @include listInLine;
            li {
                margin: 0 0.8rem;
            }
            .active {
                border-bottom: 0.3rem solid var(--primary-color);
            }
            a {
                display: inline-block;
                text-decoration: none;
                font-size: var(--font-sm);
                font-weight: 500;
                color: var(--secondary-color);
                padding: 2.7rem 0
                
            }
            .active a {
                color: var(--primary-color);
            }
        }
    }
}
    
</style>