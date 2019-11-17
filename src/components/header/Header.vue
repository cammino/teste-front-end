<template>

    <div class="header-container">

        <header>

            <div class="logo">
                <span>DEMO STORE</span>
                <img src="@/assets/image/logo.png" alt="">

            </div>

            <div class="search">
                <input type="text">
                <span class="search-icon"><i class="fa fa-search"></i></span>
            </div>

        </header>

        <Menu></Menu>

        <Slider></Slider>

    </div>

</template>

<script>

    import Menu from "@/components/header/menu/Menu"
    import Slider from "@/components/header/slider/Slider"

    export default {
        name: "Header",
        components:{
            Menu,
            Slider
        }
    }
</script>

<style lang="scss" src="./header.scss" scoped></style>