<template>
  <section class="deals">
    <div class="container">
        <div class="deals__top  d-flex flex-column flex-md-row justify-content-md-between">
            <div class="deals__header d-flex flex-column">
                <h2 class="deals__title header__title">Best Real Estate Deals</h2>
                <p class="deals__sub-title">Colonel gravity get thought fat smiling add but. Wonder twenty <br> hunted and put income set desire expect.</p>
            </div>
            <a href="#" class="deals__btn btn">View All Property</a>
        </div>

        <div class="deals__center">
            <DealsTabBlock :deals__tabs="dealsTab" :isActive="isActive" @changeIsActive="changeIsActive($event)" />
        </div>

        <div class="deals__bottom">
          <DealsListBlock :deals__list="filteredDealsList"/>
        </div>
    </div>
  </section>
</template>

<script>
import DealsTabBlock from './deals/DealsTabBlock.vue';
import DealsListBlock from './deals/DealsListBlock.vue';

export default {
    components: { DealsTabBlock, DealsListBlock },
    data () {
        return {
            isActive: 12,
            dealsTab: [
                { name: 'Residential Property', link: '#', id: 12 },
                { name: 'Commercial Property', link: '#', id: 23 },
                { name: 'Agriculture Property', link: '#', id: 34 },
                { name: 'Industrial Property', link: '#', id: 45 },
            ],
            dealsList: [
              { linkOne: '#', linkTwo: '#', linkImage: '#', img: 'home-01', id: 23, tag: 'Residential Property, Commercial Property'},
              { linkOne: '#', linkTwo: '#', linkImage: '#', img: 'home-02', id: 22, tag: 'Residential Property, Agriculture Property, Commercial Property'},
              { linkOne: '#', linkTwo: '#', linkImage: '#', img: 'home-03', id: 12, tag: 'Residential Property. Agriculture Property'},
              { linkOne: '#', linkTwo: '#', linkImage: '#', img: 'home-02', id: 45,  tag: 'Industrial Property. Agriculture Property'},
              { linkOne: '#', linkTwo: '#', linkImage: '#', img: 'home-01', id: 87,  tag: 'Industrial Property. Agriculture Property'},
            ],
        }
    },
    methods: {
         changeIsActive: function (id) {
            this.isActive = id;
         },
    },
    computed: {
      filteredDealsList() {
        let activeTags = this.dealsTab.filter(item => item.id == this.isActive)[0].name;
        return this.dealsList.filter(item =>  item.tag?.includes(activeTags));
      }
    }
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";

.deals {
    padding: 125px 0;

    .deals__top {
        margin-bottom: 50px;
    }

    .deals__title {
      margin-bottom: 15px;
    }

    .deals__sub-title {
      margin-bottom: 0;
      line-height: 150%;
      color: #000000;
    }

    .deals__btn {
      padding: 22px 34px; 
      height: 65px;
      border-radius: 5px;
      box-shadow: 0px 100px 80px rgba(248, 90, 71, 0.07),
                  0px 64.8148px 46.8519px rgba(248, 90, 71, 0.0531481), 
                  0px 38.5185px 25.4815px rgba(248, 90, 71, 0.0425185), 
                  0px 20px 13px rgba(248, 90, 71, 0.035), 
                  0px 8.14815px 6.51852px rgba(248, 90, 71, 0.0274815), 
                  0px 1.85185px 3.14815px rgba(248, 90, 71, 0.0168519);
    }

    @media (max-width: $lg-width) {
      padding: 60px 0;
    }

    @media (max-width: $md-width) {
      padding: 60px 0;

      .deals__sub-title {
        margin-bottom: 15px;
      }
    }

    @media (max-width: $md-width) {
      padding-top: 10px;
      padding-bottom: 30px;
    }

}

</style>