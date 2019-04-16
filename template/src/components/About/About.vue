<template>
    <div class="about-page">
        <div class="about">
            <h1>Информация</h1>
            <h3>ORDA CUP</h3>
            <h3>32 команд</h3>
            <h3>500 000 тг</h3>
        </div>
    </div>
</template>
<style lang="stylus" scoped>
.about-page{
    background-image url('/img/About.jpg')
    background-size cover
    background-position center
    background-repeat no-repeat
    height 100vh
    width 100%
    position relative
}
.about{
    color #fff;
    position absolute
    left 50%
    top 20%
}
.about h1{
    font-size 2.8rem
    margin-bottom 100px
}
.about h3{
    color #ECAA00;
    margin-top 20px
    font-size 2.3rem
}
@media (min-width: 481px) and (max-width: 850px) and (orientation: landscape){
    .about h1{
        font-size 2rem
        margin-bottom 40px
    }
    .about h3{
        color #ECAA00;
        margin-top 10px
        font-size 1.7rem
    }
}
@media (min-width: 320px) and (max-width: 480px) {
    .about{
        left 40%
    }
    .about h1{
        font-size 1.7rem
        margin-bottom 40px
    }
    .about h3{
        color #ECAA00;
        margin-top 10px
        font-size 1.5rem
    }
}
</style>
