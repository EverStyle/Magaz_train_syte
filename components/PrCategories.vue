<template>
  <b-container class="bv-example-row">
    <b-row>
      <b-col class="border" cols="12" sm="12" md="6" lg="6" xl="3">
        Search
        <div class="dropdown_1">
          <b-dropdown variant="light" style="width: 250px" :text="dropdown_1">
            <b-dropdown-item
              style="width: 250px"
              @click="swit(sell.name,1)"
              v-for="sell in sellvar"
              :key="sell"
            >{{sell.name}}</b-dropdown-item>
          </b-dropdown>
        </div>
      </b-col>
      <b-col class="border" cols="12" sm="12" md="6" lg="6" xl="3">
        Product category
        <div class="dropdown_2">
          <b-dropdown variant="light" style="width: 250px" :text="dropdown_2">
            <b-dropdown-item
              style="width: 250px"
              @click="swit(sell.name,2)"
              v-for="sell in sellvar2"
              :key="sell"
            >{{sell.name}}</b-dropdown-item>
          </b-dropdown>
        </div>
      </b-col>
      <b-col class="border" cols="12" sm="12" md="6" lg="6" xl="3">
        Sale
        <div class="dropdown_3">
          <b-dropdown variant="light" style="width: 250px" :text="dropdown_3">
            <b-dropdown-item
              style="width: 250px;"
              @click="swit(sell.name,3)"
              v-for="sell in sellvar3"
              :key="sell"
            >{{sell.name}}</b-dropdown-item>
          </b-dropdown>
        </div>
      </b-col>
      <b-col class="border" cols="12" sm="12" md="6" lg="6" xl="3">
        <div class="dropdown">
          <div class="empty_space" style="height: 20px"></div>
          <b-button
            @click="ChooseCat"
            style="width: 200px; height: 40px; background-color: black; "
          >Apply</b-button>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      dropdown_1: "Choose category",
      dropdown_2: "Choose category",
      dropdown_3: "Choose category"
    };
  },
  methods: {
    ChooseCat() {},

    swit(name, number) {
      switch (number) {
        case 1:
          this.dropdown_1 = name;
          break;
        case 2:
          this.dropdown_2 = name;
          break;
        case 3:
          this.dropdown_3 = name;
          break;
      }
      this.$emit('setFilter',{name, number});
    }
  },

  props: {
    sellvar: {
      type: Array,
      required: true
    },
    sellvar2: {
      type: Array,
      required: true
    },
    sellvar3: {
      type: Array,
      required: true
    }
  },
  mounted() {
    console.log(this.sellvar);
  }
};
</script>

<style>
</style>