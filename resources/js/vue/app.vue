<template>
    <div>
        <Header/>
        <Carousel/>
        <Footer/>
    </div>
</template>

<script>
import Header from "../components/Header";
import Footer from "../components/Footer";
import Carousel from "../components/Carousel";
export default {
    name: 'app',
    components: {
        Carousel,
        Footer,
        Header,
    },
}
</script>

<style lang="scss">

</style>
