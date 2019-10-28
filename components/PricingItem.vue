<template>
  <div class="pricing-item">
    <p class="pricing-item__title" @click="showBind">
      {{offer.name}}
      <svg class="icon" :class="{'icon--rotate': show}">
        <use xlink:href="#1208065781571662045" />
      </svg>
    </p>
    <transition name="list" mode="out-in">
      <ul class="pricing__list" v-if="show">
        <li class="pricing__item" v-for="item in offer.values" :key="item.name">
          {{item.name}}
          <span class="pricing__price">from ${{item.price}}</span>
        </li>
      </ul>
    </transition>
  </div>
</template>

<script>
export default {
  name: "PricingItem",
  props: {
    offer: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      show: false
    };
  },
  methods: {
    showBind() {
      this.show = !this.show;
    }
  }
};
</script>