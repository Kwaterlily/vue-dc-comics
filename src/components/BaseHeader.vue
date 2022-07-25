<template>
    <div id="header">
        <figure>
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="dc-comics" />
            </a>
        </figure>
        <nav class="header-nav">
            <ul>
                <li v-for="(link, index) in headerLinks" :key="index" :class="{ active: link.current}">
                    <a :href="link.url">{{link.text}}</a>
                </li>
                
            </ul>
        </nav>
    </div>
</template>




<script>
export default {
    name: 'BaseHeader',
    methods: {
        activeSet(index) {
            if (this.menuLink[index].active) {
                console.log(':)')
            } else {
                for (let i = 0; i < this.menuLink.length; i++) {
                    this.menuLink[i].active = false
                }
                this.menuLink[index].active = true
            }
        }
    },
    data() {
        return {
            menu: [
         {
            text: 'Characters',
            url: '#',
            current: false,
        },
        {
            text: 'Comics',
            url: '#',
            current: true,
        },
        {
            text: 'Movies',
            url: '#',
            current: false,
        },
        {
            text: 'TV',
            url: '#',
            current: false,
        },
        {
            text: 'Games',
            url: '#',
            current: false,
        },
        {
            text: 'Collectibles',
            url: '#',
            current: false,
        },
        {
            text: 'Videos',
            url: '#',
            current: false,
        },
        {
            text: 'Fans',
            url: '#',
            current: false,
        },
        {
            text: 'News',
            url: '#',
            current: false,
        },
        {
            text: 'Shop',
            url: '#',
            current: false,
        },
        ]
  
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
#header{
    @include container;
    @include d-flex(space-between, center);
    height: 15vh;
    nav.header-nav{
        
        height: 100%;
        ul{
            height: 100%;
            @include d-flex(center, '');
            li{
                margin-left: 2rem;
                height: 100%;
                @include d-flex('', center);
                border-bottom: 4px solid transparent;
                &.active,
                &:hover{
                    border-bottom: 4px solid $secondaryColor;
                }
                a{
                    color: $fontColor;
                    text-transform: uppercase;
                    font-size: .8rem;
                }
            }
        }
    }
}
</style>