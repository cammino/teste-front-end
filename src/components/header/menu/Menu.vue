<template>

    <nav :class="['menu', {active}]">
        <button class="btn-menu" @click="toggle">
            <i class="fa fa-bars"></i>
        </button>
        <ul>
            <li><a href="#">NOVIDADES</a></li>
            <li><a href="#">BLUSAS</a></li>
            <li><a href="#">CALÇAS</a></li>
            <li><a href="#">CASACOS</a></li>
            <li><a href="#">MACACÕES</a></li>
            <li><a href="#">SAIAS</a></li>
            <li><a href="#">SHORTS</a></li>
            <li><a href="#">VESTIDOS</a></li>
            <li><a href="#">OUTLET</a></li>
        </ul>

    </nav>

</template>

<script>
    export default {
        name: "Menu",
        data(){
            return {
                active: false
            }
        },
        methods: {
            toggle(){
                return this.active = !this.active;
            }
        }
    }
</script>

<style scoped lang="scss" src="./menu.scss"></style>