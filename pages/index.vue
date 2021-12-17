<template>
  <div>
    <PrHeader />
    <PrCategories v-bind:sellvar="sellvar" v-bind:sellvar2="sellvar2" v-bind:sellvar3="sellvar3" @setFilter="activeFilters=$emit"/>
    <PrCardList v-bind:cards="cards" @sendId="showConsole" />
    <PrCart v-if="" />
  </div>
</template>

<script>
import PrHeader from "@/components/PrHeader";
import PrCategories from "@/components/PrCategories";
import PrCardList from "@/components/PrCardList";
import PrCart from "@/components/PrCart";
export default {
  methods: {
    showConsole(data){
      console.log(data)
    }
  },

  components: {
    PrHeader,
    PrCategories,
    PrCardList,
    PrCart
  },
  data() {
    return {
      activeFilters:{}

      ,
      cards: [
        { id: 1, cat: "Converse",title: "Kids 70", price: "$49.99", src: "bb.png",discount: ''},
        { id: 2, cat: "Converse", title: "Chuck 70", price: "$39.99", src: "bb.png",discount: 30 },
        {
          id: 3, cat: "Converse",
          title: "Kids 70 Renew High Top",
          price: "$50.99",
          src: "bb.png"
        },
        { id: 4,  cat: "Converse", title: "pro 70", price: "$39.99", src: "bb.png", discount: 40},
        { id: 5, cat: "Converse", title: "Kids 70", price: "$49.99", src: "bb.png",discount: ''},
        { id: 6, cat: "Converse", title: "Chuck 70", price: "$39.99", src: "bb.png",discount: 30 },
        {
          id: 7,  cat: "Converse",
          title: "Kids 70 Renew High Top",
          price: "$50.99",
          src: "bb.png"
        },
        { id: 8,  cat: "Converse", title: "pro 70", price: "$39.99", src: "bb.png", discount: 40},
        { id: 9, cat: "Reverse", title: "Kids 70", price: "$49.99", src: "bb.png",discount: ''},
        { id: 10, cat: "Reverse", title: "Chuck 70", price: "$39.99", src: "bb.png",discount: 30 },
        {
          id: 11,  cat: "Reverse",
          title: "Kids 70 Renew High Top",
          price: "$50.99",
          src: "bb.png"
        },
        { id: 12,  cat: "Reverse", title: "pro 70", price: "$39.99", src: "bb.png", discount: 40},

      ],

      sellvar: [
        { name: "Converse", value: 1 },
        { name: "Reverse", value: 2 },
        { name: "Standart", value: 3 },
        { name: "Special", value: 4 }
      ],
       sellvar2: [
        { name: "Sneakers", value: 1 },
        { name: "Boots", value: 2 },
        { name: "Cross boots", value: 3 },
        { name: "Shoes", value: 4 }
      ],
       sellvar3: [
        { name: "Bestsellers", value: 1 },
        { name: "Variant 2", value: 2 },
        { name: "Variant 3", value: 3 },
        { name: "Variant 4", value: 4 }
      ],
      
    };
  }
};
</script>


<style>
</style>

