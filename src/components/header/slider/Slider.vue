<template>

    <div class="slider">

        <transition name="fade" tag="div">

            <div v-for="i in [currentIndex]" :key="i">
                <img :src="currentImage" alt=""/>
            </div>

        </transition>

        <div class="navigation-buttons">
            <button class="btn-prev" @click="prev()">&#10094;</button>
            <button class="btn-next" @click="next()">&#10095;</button>
        </div>

    </div>

</template>

<script>
    export default {
        name: "slider",
        data(){
            return {
                images: [
                    "https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg",
                    "https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg",
                    "https://cdn.pixabay.com/photo/2015/05/15/14/27/eiffel-tower-768501_1280.jpg",
                    "https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg"
                ],
                currentIndex: 0
            }
        },
        mounted() {
            this.runSlide();
        },
        methods: {
            runSlide() {
                setInterval(this.next, 4000);
            },
            next() {
                this.currentIndex += 1;
            },
            prev() {
                this.currentIndex -= 1;
            }
        },

        computed: {
            currentImage() {
                return this.images[Math.abs(this.currentIndex) % this.images.length];
            }
        }
    }
</script>

<style lang="scss"  src="./slider.scss" scoped></style>