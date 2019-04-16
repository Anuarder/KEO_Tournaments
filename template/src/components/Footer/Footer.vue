<template>
    <div class="footer-page">
        <div class="title">
            Контакты
        </div>
        <div class="footer">
            <div class="icons">
                <img src="/img/keo.png" class="keo">
                <img src="/img/orda.png" class="orda">
            </div>
            <div class="keo-address">
                <div>
                    <div class="address">
                        <h5>Keo GG</h5>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            Almaty, Al-Farabi avenue, 144
                        </div>
                    </div>
                    <div class="phone">
                        <i class="fas fa-phone"></i>
                        <a href="tel:+77771234567">
                            +7 777 123 4567
                        </a>
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
                </div>
            </div>
            <div class="orda-address">
                <div>
                    <div class="address">
                        <h5>Orda</h5>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            Almaty, Al-Farabi avenue, 144
                        </div>
                    </div>
                    <div class="phone">
                        <i class="fas fa-phone"></i>
                        <a href="tel:+77771234567">
                            +7 777 123 4567
                        </a>
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
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="stylus" scoped>
.footer-page{
    background-color #000
    height 400px
    width 100%
}
.title{
    color #fff
    font-size 1.2rem
    text-align center
    padding-top 50px
}
.footer{
    display flex
    justify-content center
}
.icons{
    display flex
    flex-direction column
    align-items center
    .keo{
        width 229px
        height 85px
    }
    .orda{
        width 167px
        height 163px
    }
}

address(){
    color #fff
    font-size 1.3rem
    display flex
    flex-direction column
    justify-content center
    h5{
        color #ECAA00
        font-size 1.3rem
        padding-bottom 1.5rem
    }
    .address, .phone{
        margin-top 1.1rem
        i{
            color #ECAA00
            margin-right 1rem
        }
    }
    a{
        color #fff
    }
}
.keo-address{
    address()
    margin 0 80px 0 140px
}
.orda-address{
    address()
}
.social-links{
    display flex
    align-items center
    margin-top 30px
    .social-link{
        font-size 1.5rem
        margin-left 1.4rem
    }
}
@media (min-width: 481px) and (max-width: 850px) and (orientation: landscape){
    .title{
        font-size 2rem
    }
    .footer-page{
        height 100%
    }
    .footer{
        display flex
        flex-direction column
        justify-content center
    }
    .icons{
        flex-direction row
        justify-content center
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
    .keo-address{
        margin 0
        align-items center
    }
    .orda-address{
        margin 40px 0
        align-items center
    }
}
@media (max-width: 768px) {
    .title{
        font-size 2rem
    }
    .footer-page{
        height 100%
    }
    .footer{
        display flex
        flex-direction column
        justify-content center
    }
    .icons{
        flex-direction row
        justify-content center
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
    .keo-address{
        margin 0
        align-items center
    }
    .orda-address{
        margin 40px 0
        align-items center
    }
}
@media (max-width: 320px) {
    .keo-address, .orda-address{
        font-size 1rem
    }
}
</style>
