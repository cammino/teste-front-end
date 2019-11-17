<template >

  <div class="home">
      <section>
          <h1>Ofertas em destaque</h1>
          <OffersCard v-for="card in cardData" :key="card.id" :cardData="card"></OffersCard>
      </section>
  </div>

</template>

<script>

import OffersCard from "@/components/offers_card/OffersCard";

export default {
  name: 'home',
  components:{
    OffersCard
  },
    data(){
      return{
          cardData: [
              {
                  id: 1,
                  offerTip: '10% OFF',
                  src: require('@/assets/image/product-1.jpeg'),
                  title: 'Neon Bluetooth Wirelles On-Ear Headphones',
                  depreciatedPrice: 'R$ 18,90',
                  spotPrice: 'R$ 14,90',
                  fowardPrice: 'ou 6x de R$ 4,50'
              },
              {
                  id: 2,
                  offerTip: null,
                  src: require('@/assets/image/product-2.jpeg'),
                  title: 'PC-All in one',
                  depreciatedPrice: 'R$ 3.230,90',
                  spotPrice: 'R$ 2.100,90',
                  fowardPrice: 'ou 12x de R$ 210,00'
              },
              {
                  id: 3,
                  offerTip: null,
                  src: require('@/assets/image/product-3.jpeg'),
                  title: 'Samsung Galaxy A7',
                  depreciatedPrice: 'R$ 1.650,00',
                  spotPrice: 'R$ 875,99',
                  fowardPrice: 'ou 12x de R$ 91,50'
              },
              {
                  id: 4,
                  offerTip: '12% OFF',
                  src: require('@/assets/image/product-4.jpeg'),
                  title: 'Smart TV 62"',
                  depreciatedPrice: 'R$ 3.790,00',
                  spotPrice: 'R$ 2.300,00',
                  fowardPrice: 'ou 12x de R$ 230,00'
              },
              {
                  id: 5,
                  offerTip: null,
                  src: require('@/assets/image/product-5.jpeg'),
                  title: 'Notebook Aio',
                  depreciatedPrice: 'R$ 3.350,00',
                  spotPrice: 'R$ 2.000,00',
                  fowardPrice: 'ou 12x de R$ 200,00'
              },
              {
                  id: 6,
                  offerTip: '19% OFF',
                  src: require('@/assets/image/product-6.jpeg'),
                  title: 'Notebook Aio',
                  depreciatedPrice: 'R$ 3.350,00',
                  spotPrice: 'R$ 2.000,00',
                  fowardPrice: 'ou 12x de R$ 200,00'
              }

          ]
      }
    }
}
</script>

<style scoped lang="scss" src="./home.scss"></style>
