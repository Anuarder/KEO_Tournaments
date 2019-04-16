<template>
    <div class="commands-page">
        <router-link to="/">
            <div class="arrow-back">
                <img src="/img/back.svg">
                назад
            </div>
        </router-link>
        <router-link to="/">
            <div class="header">
                <div class="logo">
                    <div class="keo">
                        <img src="/img/keo.png" alt="">
                    </div>
                    <div class="orda">
                        <img src="/img/orda.png" alt="">
                    </div>
                </div>
            </div>
        </router-link>
        <div class="main">
            <h1>Составы команд</h1>
            <div class="commands">
                <div 
                    v-for="(item, i) in commands"
                    :key="i"
                    class="command">
                    <div class="name">
                        <h2>
                            {{item.name}}
                        </h2>
                        <h3 class="subheader">
                            Список игроков:
                        </h3>
                    </div>
                    <div class="players-list">
                        <div 
                            v-for="(player, j) in item.players"
                            :key="j"
                            class="player">
                            <img src="/img/player.svg">
                            {{player.name}}
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer">
            <keo-footer></keo-footer>
        </div>
    </div>
</template>
<script>
import KeoFooter from '../components/Footer/Footer'
export default {
    components:{
        KeoFooter
    },
    data(){
        return {
            commands: [
                {
                    name: 'Collaps',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
                {
                    name: 'Super Mega Brothers',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
                {
                    name: 'Babao',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
                {
                    name: 'RUSK',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
                {
                    name: 'AIM',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
                {
                    name: 'LOLOLO',
                    players: [
                        {
                            name: 'Jose R. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose A. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose B. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose V. “Nickname” Barefield',
                        },
                        {
                            name: 'Jose D. “Nickname” Barefield',
                        },
                    ]
                },
            ]
        }
    }
}
</script>
<style lang="stylus" scoped>
.arrow-back{
    position absolute
    top 70px
    left 2%
    display flex
    align-items center
    color #ECAA00
    font-size 1.3rem
    font-weight thin
    img{
        padding-right .6rem
    }
}
.commands-page{
    height 100%
    width 100%
    background: linear-gradient(75.01deg, #22222C 2.72%, #080B0D 75.79%);
    display flex
    flex-direction column
}
.logo{
    display flex
    justify-content center
    align-items center
    padding 20px 0
    
    .orda{
        padding-left 60px
    }
    img{
        max-width 80%
    }
}

.main{
    flex 1
    min-height 100vh
}
.main{
    color #fff
    h1{
        margin-top 50px
        font-size 2.5rem
        text-align center
    }
}
.commands{
    max-width 1200px;
    margin 0 auto
    display: grid;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 100px;
    width: 100%;
    height: 100%;
    margin-top 80px
}
.command{
    box-sizing: border-box;
}
.name{
    padding-left 20px
    border-left 3px solid #ECAA00
    h2{
        font-size 1.5rem
        color #ECAA00
    }
    h3{
        margin-top 5px
        font-size 1.1rem
        font-weight normal
    }
}
.players-list{
    font-size 1.1rem
    margin-top 40px
}
.player{
    margin-top 10px
    width 100%
    height: 100%;
    img{
        padding-right .5rem
    }
}

@media (max-width: 1439px) {
    .commands{
        max-width 1000px
    }
}
@media (max-width: 1024px) {
    .arrow-back{
        display none
    }
    .commands{
        max-width 900px
    }
    .name{
        h2{
            font-size 1.1rem
        }
        h3{
            margin-top 5px
            font-size 1rem
        }
    }
    .players-list{
        font-size 1rem
        margin-top 20px
    }
    .player{
        margin-top 7px
        img{
            padding-right .3rem
        }
    }
}
@media (max-width: 850px) {
    .main{
        h1{
            margin-top 20px
            font-size 2rem
        }
    }
    .commands{
        margin-top 50px
        max-width 500px
        grid-template-rows 1fr 1fr
        grid-template-columns 1fr 1fr
        grid-gap 30px
        padding-bottom 50px
    }
    .name{
        h2{
            font-size 1rem
        }
        h3{
            margin-top 5px
            font-size 1rem
        }
    }
    .players-list{
        font-size 1rem
        margin-top 20px
    }
    .player{
        margin-top 7px
        img{
            padding-right .3rem
        }
    }
}
@media (min-width: 320px) and (max-width: 480px) {
    .logo{
        .orda{
            width 92px
            height 89px
        }
        .keo{
            width 127px
            height 47px
        }
        img{
            max-width 70%
        }
    }
    .main{
        h1{
            margin-top 20px
            font-size 2rem
        }
    }
    .commands{
        max-width 250px
        grid-template-rows 1fr
        grid-template-columns 1fr
        grid-gap 40px
    }
    .name{
        h2{
            font-size 1rem
        }
        h3{
            margin-top 5px
            font-size 1rem
        }
    }
    .players-list{
        font-size 1rem
        margin-top 20px
    }
    .player{
        margin-top 7px
        img{
            padding-right .3rem
        }
    }
}

</style>

