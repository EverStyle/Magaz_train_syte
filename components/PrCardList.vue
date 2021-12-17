<template>
  <b-container class="bv-example-row" style="padding-top:20px">
    <div class="main_title">BestSellers</div>

    <b-row>
      <b-col class="border" cols="12" sm="12" md="12" lg="12" xl="12">
        <div class="main" v-for="main in cards" :key="main.id">
          <div class="img_block">
            <img class="img_card" :src="'img/' + main.src" alt="error" />
            <div v-if="main.discount" class="img_discount">Sale {{main.discount}} %</div>
          </div>
          <div class="main_title">{{main.cat}} {{main.title}}</div>
          <div class="main_price">{{main.price}}</div>
          <div class="add_button">
            <b-button @click="sendData(main.id)" style="width: 100%; height: 40px; background-color: black; ">Add to basket</b-button>
          </div>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  props: {
    cards: {
      type: Array,
      required: true
    }
  },
  methods:{
    sendData(id){
      this.$emit('sendId',id)
    }
  }
};
</script>

<style>
.main{
  display: inline-block;
  flex-wrap: wrap;
  padding-right: 15px;
}
.img_block{
  position: relative;
}
.img_card{
  max-width: 300px;
  max-height: 380px;
  width: 250px;
  height: 300px;
  
}
.main_title{

}
.main_price{
padding-bottom: 10px;
}
</style>