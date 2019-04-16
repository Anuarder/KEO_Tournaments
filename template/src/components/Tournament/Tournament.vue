<template>
    <div class="tournament-page" id="tournaments">
        <div class="tournament">
            <div class="title">
                <h1>Турнирная таблица</h1>
            </div>
            <div class="tournament-table">
                <iframe 
                    src="https://challonge.com/7vgmcgsj/module?theme=1&multiplier=1&tab=final" 
                    frameborder="0" 
                    scrolling="auto"
                    allowtransparency="false">
                </iframe>
            </div>
        </div>
    </div>
</template>
<style lang="stylus" scoped>
.tournament-page{
    background-image url('/img/TOURNAMENT.jpg')
    background-size cover
    background-position center
    background-repeat no-repeat
    height 100vh
    width 100%
}
.title{
    text-align center
    color #fff
    font-size 1.5rem
    padding-top 70px
}
.tournament{
    display flex
    flex-direction column
    height 100%
}
.tournament-table{
    flex 1
    margin-top 50px
    width 100%
    height auto
    iframe{
        width 100%
        height 100%
    }
}
@media (min-width: 481px) and (max-width: 850px) and (orientation: landscape){
    .title{
        font-size 1.2rem
        padding-top 50px
    }
}
@media (min-width: 320px) and (max-width: 480px) {
   .title{
        font-size 1.1rem
        padding-top 50px
    } 
}
</style>
