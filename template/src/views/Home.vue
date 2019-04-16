<template>
    <div class="home">
        <keo-header></keo-header>
        <div class="grad"></div>
        <keo-about></keo-about>
        <div class="grad"></div>
        <keo-tournament></keo-tournament>
        <div class="grad"></div>
        <keo-footer></keo-footer>
    </div>
</template>
<script>
import KeoHeader from '../components/Header/Header'
import KeoAbout from '../components/About/About'
import KeoTournament from '../components/Tournament/Tournament'
import KeoFooter from '../components/Footer/Footer'
export default {
    components: {
        KeoHeader,
        KeoAbout,
        KeoTournament,
        KeoFooter
    }
}
</script>