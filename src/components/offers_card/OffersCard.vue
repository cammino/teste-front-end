<template>
    <!--CARD 1-->
    <div class="card">

        <div class="card-header">

            <template v-if="cardData.offerTip != null">
                <strong class="offer-tip">{{ cardData.offerTip }}</strong>
            </template>

            <img :src="cardData.src" alt="">
            <div class="cover"></div>

        </div>

        <h2 class="card-title">{{ cardData.title }}</h2>

        <div class="card-body">

            <div class="average-rater">

                <i class="fa fa-star active"></i>
                <i class="fa fa-star active"></i>
                <i class="fa fa-star active"></i>
                <i class="fa fa-star active"></i>
                <i class="fa fa-star"></i>

            </div>

            <div class="price-type">
                <strong class="through-pice">
                    {{ cardData.depreciatedPrice }}
                </strong>
                <span>|</span>
                <strong class="spot-price">
                   {{ cardData.spotPrice }}
                </strong>
            </div>


            <strong class="foward-price">
                {{ cardData.fowardPrice }}
            </strong>

        </div>

        <div class="card-footer">
            <button class="btn-purchase">COMPRAR</button>
        </div>

    </div>

</template>

<script>
    export default {
        name: "OffersCard",
        props: {
            cardData:{type: Object}
        }
    }
</script>

<style lang="scss" src="./offers_card.scss" scoped></style>