<template>
    <div class="header">
        <div class="logo">
            <div class="keo">
                <img src="/img/keo.png" alt="">
            </div>
            <div class="orda">
                <img src="/img/orda.png" alt="">
            </div>
        </div>
        <div class="video-wrap">
            <div class="video">
                <div class="video-player">
                    <keo-tube 
                        v-if="youtube && !twitch">
                    </keo-tube>
                    <keo-twitch 
                        v-if="twitch && !youtube">
                    </keo-twitch>
                </div>
            </div>
            <div class="video-controls">
                <div class="controls">
                    <div class="switch-buttons">
                        <button 
                            :class="getActive == 'youtube' ? 'active' : ''"
                            class="switch-button youtube" 
                            @click="setPlayer('youtube')">
                            YouTube
                        </button>
                        <button 
                            :class="getActive == 'twitch' ? 'active' : ''"
                            class="switch-button twitch"
                            @click="setPlayer('twitch')">
                            Twitch
                        </button>
                    </div>
                </div>
            </div>
        </div>
        <div class="social-links">
            <a href="#" class="social-link">
                <i class="fab fa-twitch"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fab fa-vk"></i>
            </a>    
            <a href="#" class="social-link">
                <i class="fab fa-youtube"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fab fa-instagram"></i>
            </a>
        </div>  
        <div class="link-wrap">
            <div class="buttons-container">
                <div class="tournaments-btn-container">
                    <a href="#tournaments" class="tournaments-btn">
                        Перейти к сетке
                    </a>
                </div>
                <div class="commands-btn-container">
                    <router-link to='/commands' class="commands-btn">
                        Составы команд
                    </router-link>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import KeoTube from './Players/YouTube'
import KeoTwitch from './Players/Twitch'
export default {
    components: {
        KeoTube,
        KeoTwitch
    },
    data(){
        return {
            youtube: true,
            twitch: false,
            activePlayer: 'youtube'
        }
    },
    computed: {
        getActive(){
            return this.activePlayer;
        }
    },
    methods: {
        setPlayer(player){
            if(player == 'youtube'){
                this.twitch = false;
                this.youtube = true;
            }else{
                this.youtube = false;
                this.twitch = true;
            }
            this.activePlayer = player;
        },
    }
}
</script>

<style lang="stylus" scoped>
.header{
    background-image url('/img/Header.jpg')
    background-position center
    background-size cover
    height 100vh
    width 100%
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
.video{
    display flex
    justify-content center
    .video-player{
        width 900px
        height 500px
    }
}
.video-controls{
    display flex
    justify-content center
    .controls{
        width 900px
        display flex
        justify-content flex-end
    }
}
.switch-buttons{
    padding-top .8rem
}
.switch-button{
    outline none
    cursor pointer
    background-color transparent
    color #ECAA00
    border none
    padding-right 1rem 
    font-size 1.1rem
    font-weight 600
    font-family 'Supermolot'
}
.active{
    color #fa7000
}
.social-links{
    position absolute 
    display flex
    flex-direction column
    align-items center
    top 50%
    right 70px
    transform translateY(-50%)

    .social-link{
        font-size 1.5rem
        color #fff
        padding-top 20px 
    }
}
.link-wrap{
    margin-top 50px
    display flex
    justify-content center
}
.tournaments-btn{
    display flex
    justify-content center
    align-items center
    cursor pointer
    outline none
    width: 260px;
    height: 61px;
    color #000
    font-family 'Supermolot', sans-serif;
    font-size 1.4rem
    font-weight 600
    border-radius 5px
    border none
    background-color #ECAA00
    &:hover{
        opacity .9
    }
    &:active{
        opacity 1
    }
}
.commands-btn-container{
    margin-top 25px
    text-align center
    .commands-btn{
        border-bottom 1.5px solid #fff
        color #fff
        font-weight 600
        font-size 1.5rem
    }
}
@media (max-width: 1919px){
    .video{
        .video-player{
            width 700px
            height 400px
        }
    }
    .video-controls{
        .controls{
            width 700px
        }
    }
    .link-wrap{
        margin-top 45px
    }
}

@media (max-width: 1024px) and (orientation: portrait){ 
    .social-links{
        position static 
        display flex
        flex-direction row
        justify-content center
        margin-top 50px
        .social-link{
            font-size 1.5rem
            color #fff
            padding-top 0
            padding-right 30px 
        }
    }
    .commands-btn-container{
        margin-top 40px
        .commands-btn{
            font-size 2rem
        }
    }
}
@media (max-width: 1024px) and (orientation: landscape){ 
    .logo{
        display flex
        justify-content center
        align-items center
        padding 20px 0
        .orda{
            padding-left 20px
        }
        img{
            max-width 60%
        }
    }
}
@media (max-width: 768px) { 
    .social-links{
        position static 
        display flex
        flex-direction row
        justify-content center
        margin-top 50px
        .social-link{
            font-size 1.5rem
            color #fff
            padding-top 0
            padding-right 30px 
        }
    }
}

@media (min-width: 568px) and (max-width: 850px) and (orientation: landscape){ /* Mobile landscape*/
    .video{
        .video-player{
            width 400px
            height 200px
        }
    }
    .video-controls{
        .controls{
            width 400px
        }
    }
    .link-wrap{
        margin-top 0
    }
    .logo{
        display flex
        justify-content center
        align-items center
        padding 5px 0
        .keo{
            width 136px
            margin-right 30px
        }
        .orda{
            width 99px
        }
    }
    .social-links{
        position absolute 
        display flex
        flex-direction column
        align-items center
        top 30%
        right 10px
        transform translateY(-30%)
        .social-link{
            font-size 1.1rem
            padding-top 15px 
        }
    }
    .commands-btn-container{
        margin-top 10px
        .commands-btn{
            font-size .8rem
        }
    }
    .tournaments-btn{
        display none
    }
}
@media (min-width: 320px) and (max-width: 480px) { /* Mobile portrait*/
    .video{
        .video-player{
            width 90%
            height 200px
        }
    }
    .video-controls{
        .controls{
            width 400px
        }
    }
    .link-wrap{
        margin-top 0
    }
    .logo{
        display flex
        justify-content center
        align-items center
        padding 5px 0
        .keo{
            width 136px
            height 50px
            margin-right 30px
        }
        .orda{
            width 99px
            height 97px
        }
    }
    .social-links{
        position static 
        display flex
        flex-direction row
        justify-content center
        margin-top 50px
        .social-link{
            font-size 1.5rem
            color #fff
            padding-top 0
            padding-right 30px 
        }
    }
    .commands-btn-container{
        margin-top 30px
        .commands-btn{
            font-size 1rem
        }
    }
    .tournaments-btn-container{
        margin-top 20px
    }
    .tournaments-btn{
        width: 150px;
        height: 45px;
        font-size 1rem
        background-color #ECAA00
    }
}
</style>