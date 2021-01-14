<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <!-- jumbotron  -->
    <div class="slider-area">
      <div class="slider-active owl-carousel nav-style-1  owl-dot-none">
        <div
          class="single-slider-2 slider-height-2 d-flex align-items-center bg-img"
          style="background-image:url(assets/img/slider/slider-2.jpg);"
        >
          <div class="container">
            <div class="row">
              <div class="col-xl-6 col-lg-7 col-md-8 col-12 ml-auto">
                <div class="slider-content-3 slider-animated-1 text-center">
                  <h3 class="animated"><strong>Plan</strong></h3>
                  <h1 class="animated"><strong>Your Next Event</strong></h1>
                  <h1 class="animated"><strong>Now</strong></h1>
                  <div class="slider-btn btn-hover">
                    <a class="animated" href="">SHOP NOW</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="single-slider-2 slider-height-2 d-flex align-items-center bg-img"
          style="background-image:url(assets/img/slider/slider-3.jpg);"
        >
          <div class="container">
            <div class="row">
              <div class="col-xl-6 col-lg-7 col-md-8 col-12 ml-auto">
                <div class="slider-content-3 slider-animated-1 text-center">
                  <h3 class="animated"><strong>We're</strong></h3>
                  <h1 class="animated"><strong>Happy</strong></h1>
                  <h3 class="animated"><strong>To Help</strong></h3>
                  <div class="slider-btn btn-hover">
                    <a class="animated" href="">SHOP NOW</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- cards section  -->
    <div class="product-area pb-60 section-padding-1">
      <div class="container-fluid">
        <div class="section-title-2 text-center mb-60">
          <h2>All Products</h2>
          <p>Lorem ipsum dolor sit amet conse ctetu.</p>
        </div>
        <div class="custom-row">
          <div class="custom-col-5" v-for="product in products" v-bind:key="product.id">
            <div class="product-wrap-2 mb-25 scroll-zoom">
              <div class="product-img">
                <router-link v-bind:to="`/products/${product.id}`">
                  <img class="default-img" v-bind:src="`${product.image_url}`" alt="" />
                  <img class="hover-img" v-bind:src="`${product.image_url}`" alt="" />
                </router-link>
                <!-- add discount here <span class="pink"></span> -->
                <div class="product-action-2">
                  <!-- <a title="Add To Cart" href="#"><i class="fa fa-shopping-cart"></i></a> -->
                  <!-- <a title="Quick View" href="#" data-toggle="modal" data-target="#exampleModal">
                    <i class="fa fa-eye"></i>
                  </a> -->
                </div>
              </div>
              <div class="product-content-2">
                <div class="title-price-wrap-2">
                  <h3>
                    <router-link v-bind:to="`/products/${product.id}`">{{ product.name }}</router-link>
                  </h3>
                  <div class="price-2">
                    <span>${{ product.price }}0</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Modal ********If you want a modal it goes here********  -->
  </div>
</template>

<style></style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      message: "Rental Business App ",
      products: [],
    };
  },
  created: function() {
    axios.get("/api/products").then(response => {
      console.log("products index", response);
      this.products = response.data;
    });
  },
  methods: {},
};
</script>
