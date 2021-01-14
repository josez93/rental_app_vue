/* eslint-disable no-undef */ /* eslint-disable no-undef */
<template>
  <div id="app">
    <!-- nav-bar  -->
    <header class="header-area clearfix">
      <div class="header-top-area header-padding-2">
        <div class="container-fluid">
          <div class="header-top-wap">
            <div class="header-offer">
              <p>
                Free delivery on order over
                <span>$200</span>
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="header-area header-padding-2 sticky-bar header-res-padding clearfix">
        <div class="container-fluid">
          <div class="row">
            <div class="col-xl-2 col-lg-2 col-md-6 col-4">
              <div class="logo">
                <a href="/">
                  <img alt="" src="/assets/img/logo/logo.png" />
                </a>
              </div>
            </div>
            <div class="col-xl-8 col-lg-8 d-none d-lg-block">
              <div class="main-menu">
                <nav>
                  <ul>
                    <li>
                      <a href="/">
                        Home
                      </a>
                    </li>
                    <li>
                      <a href="/">
                        Products
                        <i class="fa fa-angle-down"></i>
                      </a>
                      <ul class="mega-menu">
                        <li>
                          <ul>
                            <li class="mega-menu-title">
                              <a>
                                <i><strong>Products</strong></i>
                              </a>
                            </li>
                            <li><a href="/products/3">Chair</a></li>
                            <li><a href="/products/4">Table</a></li>
                            <li class="mega-menu-title">
                              <a>
                                <i><strong>Tents</strong></i>
                              </a>
                            </li>
                            <li><a href="/products/9">10 x 20</a></li>
                            <li><a href="/products/10">10 x 20 with walls</a></li>
                            <li><a href="/products/11">20 x 20</a></li>
                            <li><a href="/products/12">20 x 20 with walls</a></li>
                            <li><a href="/products/13">20 x 30</a></li>
                            <li><a href="/products/14">20 x 30 with walls</a></li>
                          </ul>
                        </li>
                        <li>
                          <ul>
                            <li class="mega-menu-title">
                              <a>
                                <i><strong>Bouncy Houses</strong></i>
                              </a>
                            </li>
                            <li><a href="/products/5">Bouncy House Boy</a></li>
                            <li><a href="/products/6">Bouncy House Girl</a></li>
                            <li><a href="/products/7">Bouncy House Unicorn</a></li>
                            <li><a href="/products/8">Bouncy House Sport</a></li>
                            <!-- <li><a href="/product-details-5.html">gallery style</a></li>
                            <li><a href="/product-details-slider-box.html">Slider style</a></li>
                            <li><a href="/product-details-affiliate.html">affiliate style</a></li>
                            <li><a href="/product-details-6.html">fixed image style</a></li> -->
                          </ul>
                        </li>
                        <li>
                          <ul>
                            <li class="mega-menu-img">
                              <a href=""><img src="assets/img/banner/banner-12.png" alt="" /></a>
                            </li>
                          </ul>
                        </li>
                      </ul>
                    </li>
                    <!-- v-if="!logIn()"  -->
                    <li><a href="/signup">Sign Up</a></li>
                    <li><a href="/Login">Log In</a></li>
                    <li><a href="/Logout">Log out</a></li>
                    <li><a href="/productsnew">Add products</a></li>
                    <li><a href="/carted_products">cart</a></li>
                  </ul>
                </nav>
              </div>
            </div>
            <div class="col-xl-2 col-lg-2 col-md-6 col-8">
              <div class="header-right-wrap">
                <div class="same-style header-search">
                  <a class="search-active" href="/#"><i class="pe-7s-search"></i></a>
                  <div class="search-content">
                    <form action="#">
                      <input type="text" placeholder="Search" />
                      <button class="button-search"><i class="pe-7s-search"></i></button>
                    </form>
                  </div>
                </div>
                <div class="same-style account-satting">
                  <a class="account-satting-active" href="/"><i class="pe-7s-user-female"></i></a>
                  <div class="account-dropdown">
                    <ul>
                      <li><a href="/login">Login</a></li>
                      <li><a href="/Signup">Sign Up</a></li>
                    </ul>
                  </div>
                </div>
                <!-- <div class="same-style cart-wrap">
                  <button class="icon-cart">
                    <i class="pe-7s-shopbag"></i>
                    <span class="count-style"></span>
                  </button>
                  <div class="shopping-cart-content">
                    <ul>
                      <li class="single-shopping-cart">
                        <div class="shopping-cart-img">
                          <a href="/#"><img alt="" src="/assets/img/cart/cart-1.png" /></a>
                        </div>
                        <div class="shopping-cart-title">
                          <h4><a href="/#">T- Shart & Jeans</a></h4>
                          <h6>Qty: 02</h6>
                          <span>$260.00</span>
                        </div>
                        <div class="shopping-cart-delete">
                          <a href="/#"><i class="fa fa-times-circle"></i></a>
                        </div>
                      </li>
                      <li class="single-shopping-cart">
                        <div class="shopping-cart-img">
                          <a href="/#"><img alt="" src="/assets/img/cart/cart-2.png" /></a>
                        </div>
                        <div class="shopping-cart-title">
                          <h4><a href="/#">T- Shart & Jeans</a></h4>
                          <h6>Qty: 02</h6>
                          <span>$260.00</span>
                        </div>
                        <div class="shopping-cart-delete">
                          <a href="/#"><i class="fa fa-times-circle"></i></a>
                        </div>
                      </li>
                    </ul>
                    <div class="shopping-cart-total">
                      <h4>
                        Shipping :
                        <span>$20.00</span>
                      </h4>
                      <h4>
                        Total :
                        <span class="shop-total">$260.00</span>
                      </h4>
                    </div>
                  <div class="shopping-cart-btn btn-hover text-center">
                      <a class="default-btn" href="/cart-page.html">view cart</a>
                      <a class="default-btn" href="/checkout.html">checkout</a>
                    </div>
                  </div>
                </div> -->
              </div>
            </div>
          </div>
          <div class="mobile-menu-area">
            <div class="mobile-menu">
              <nav id="mobile-menu-active">
                <ul class="menu-overflow">
                  <li>
                    <a href="/">HOME</a>
                  </li>
                  <li>
                    <a href="/">Products</a>
                    <ul>
                      <a href="/products/3">Chairs</a>
                      <a href="/products/4">Tables</a>
                      <li>
                        <a href="">Tents</a>
                        <ul>
                          <li><a href="/products/9">Tent 10x20</a></li>
                          <li><a href="/products/10">Tent 10x20 w/walls</a></li>
                          <li><a href="/products/11">Tent 20x20</a></li>
                          <li><a href="/products/12">Tent 20x20 w/walls</a></li>
                          <li><a href="/products/13">Tent 20x30</a></li>
                          <li><a href="/products/14">Tent 20x30 w/walls</a></li>
                        </ul>
                      </li>
                      <li>
                        <a href="">Bouncy Houses</a>
                        <ul>
                          <li><a href="/products/5">Bouncy house Boy</a></li>
                          <li><a href="//products/6">Bouncy house girl</a></li>
                          <li><a href="/products/7">Bouncy house unicorn</a></li>
                          <li><a href="/products/8">Bouncy house sport</a></li>
                          <li><a href="/products/5">Bouncy house Boy</a></li>
                          <li><a href="/products/6">Bouncy house girl</a></li>
                          <li><a href="/products/7">Bouncy house unicorn</a></li>
                          <li><a href="/products/8">Bouncy house sport</a></li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                  <li><a href="/signup">Sign up</a></li>
                  <li><a href="/login">Log In</a></li>
                  <li><a href="/logout">Log Out</a></li>
                  <li><a href="/productsnew">Add Products</a></li>
                  <li><a href="/cartedproducts">cart</a></li>
                </ul>
              </nav>
            </div>
          </div>
        </div>
      </div>
    </header>
    <router-view />
    <!-- footer  -->
    <footer class="footer-area bg-gray pt-100 pb-70">
      <div class="container">
        <div class="row">
          <div class="col-lg-2 col-md-4 col-sm-4">
            <div class="copyright mb-30">
              <div class="footer-logo">
                <a href="/">
                  <img alt="" src="/assets/img/logo/logo.png" />
                </a>
              </div>
              <p>
                © 2021
                <a href="#">[YOUR LOGO HERE]</a>
                .
                <br />
                All Rights Reserved
              </p>
            </div>
          </div>
          <div class="col-lg-2 col-md-4 col-sm-4">
            <div class="footer-widget mb-30 ml-30">
              <div class="footer-title">
                <h3>ABOUT US</h3>
              </div>
              <div class="footer-list">
                <ul>
                  <li><a href="/about">About us</a></li>
                  <li><a href="#">Store location</a></li>
                  <li><a href="contact.html">Contact</a></li>
                  <li><a href="#">Orders tracking</a></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-lg-2 col-md-4 col-sm-4">
            <div class="footer-widget mb-30 ml-50">
              <div class="footer-title">
                <h3>USEFUL LINKS</h3>
              </div>
              <div class="footer-list">
                <ul>
                  <li><a href="#">Returns</a></li>
                  <li><a href="#">Support Policy</a></li>
                  <li><a href="#">Size guide</a></li>
                  <li><a href="#">FAQs</a></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-lg-2 col-md-6 col-sm-6">
            <div class="footer-widget mb-30 ml-75">
              <div class="footer-title">
                <h3>FOLLOW US</h3>
              </div>
              <div class="footer-list">
                <ul>
                  <li><a href="#">Facebook</a></li>
                  <li><a href="#">Twitter</a></li>
                  <li><a href="#">Instagram</a></li>
                  <li><a href="#">Youtube</a></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-md-6 col-sm-6">
            <div class="footer-widget mb-30 ml-70">
              <div class="footer-title">
                <h3>SUBSCRIBE</h3>
              </div>
              <div class="subscribe-style">
                <p>Get E-mail updates about our latest shop and special offers.</p>
                <div id="mc_embed_signup" class="subscribe-form">
                  <form
                    id="mc-embedded-subscribe-form"
                    class="validate"
                    novalidate=""
                    target="_blank"
                    name="mc-embedded-subscribe-form"
                    method="post"
                    action="https://devitems.us11.list-manage.com/subscribe/post?u=6bbb9b6f5827bd842d9640c82&amp;id=05d85f18ef"
                  >
                    <div id="mc_embed_signup_scroll" class="mc-form">
                      <input
                        class="email"
                        type="email"
                        required=""
                        placeholder="Enter your email here.."
                        name="EMAIL"
                        value=""
                      />
                      <div class="mc-news" aria-hidden="true">
                        <input type="text" value="" tabindex="-1" name="b_6bbb9b6f5827bd842d9640c82_05d85f18ef" />
                      </div>
                      <div class="clear">
                        <input
                          id="mc-embedded-subscribe"
                          class="button"
                          type="submit"
                          name="subscribe"
                          value="Subscribe"
                        />
                      </div>
                    </div>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<style></style>

<script>
export default {
  mounted: function() {
    (function($) {
      "use strict";

      /* Cart search */
      $(".account-satting-active , .search-active").on("click", function(e) {
        e.preventDefault();
        $(this)
          .parent()
          .find(".account-dropdown , .search-content")
          .slideToggle("medium");
      });

      /* Cart dropdown */
      var iconCart = $(".icon-cart");
      iconCart.on("click", function() {
        $(".shopping-cart-content").toggleClass("cart-visible");
      });

      /* Slider active */
      $(".slider-active").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        navText: ['<i class="fa fa-chevron-left"></i>', '<i class="fa fa-chevron-right"></i>'],
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        item: 1,
        responsive: {
          0: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });

      /* Slider active 2 */
      $(".slider-active-2").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        navText: ['<i class="pe-7s-angle-left"></i>', '<i class="pe-7s-angle-right"></i>'],
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        item: 1,
        responsive: {
          0: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });

      /* Slider active */
      $(".slider-active-3").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        item: 1,
        responsive: {
          0: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });

      /* Instagram active */
      $(".instagram-active").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        item: 5,
        responsive: {
          0: {
            items: 2,
          },
          768: {
            items: 4,
          },
          1000: {
            items: 5,
          },
        },
      });

      /* Collection slider active */
      $(".collection-active").owlCarousel({
        loop: true,
        nav: false,
        autoplay: true,
        autoplayTimeout: 5000,
        item: 4,
        margin: 30,
        responsive: {
          0: {
            items: 1,
          },
          576: {
            items: 2,
          },
          768: {
            items: 3,
          },
          1000: {
            items: 4,
          },
        },
      });

      /* Collection slider active 2 */
      $(".collection-active-2").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        item: 3,
        margin: 30,
        responsive: {
          0: {
            items: 1,
          },
          576: {
            items: 2,
          },
          768: {
            items: 3,
          },
          1000: {
            items: 3,
          },
        },
      });

      /* product-slider active */
      $(".product-slider-active").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        navText: ['<i class="fa fa-angle-left"></i>', '<i class="fa fa-angle-right"></i>'],
        autoplayTimeout: 5000,
        item: 4,
        margin: 30,
        responsive: {
          0: {
            items: 1,
            autoplay: true,
          },
          576: {
            items: 2,
          },
          768: {
            items: 2,
          },
          992: {
            items: 3,
          },
          1200: {
            items: 4,
          },
        },
      });

      /* product-slider active 2 */
      $(".product-slider-active-2").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        item: 4,
        margin: 30,
        responsive: {
          0: {
            items: 1,
            autoplay: true,
          },
          576: {
            items: 2,
          },
          768: {
            items: 2,
          },
          992: {
            items: 3,
          },
          1200: {
            items: 4,
          },
        },
      });

      /* product-slider active 3 */
      $(".product-slider-active-3").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        navText: ['<i class="fa fa-long-arrow-left"></i>', '<i class="fa fa-long-arrow-right"></i>'],
        autoplayTimeout: 5000,
        item: 4,
        margin: 30,
        responsive: {
          0: {
            items: 1,
            autoplay: true,
          },
          576: {
            items: 2,
          },
          768: {
            items: 2,
          },
          992: {
            items: 3,
          },
          1200: {
            items: 4,
          },
        },
      });

      /* Testimonial active */
      $(".testimonial-active").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        navText: ['<i class="pe-7s-angle-left"></i>', '<i class="pe-7s-angle-right"></i>'],
        autoplayTimeout: 5000,
        item: 1,
        margin: 30,
        responsive: {
          0: {
            items: 1,
            autoplay: true,
          },
          576: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });
      /* Testimonial 2 active */
      $(".testimonial-active-2").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        navText: ['<i class="pe-7s-angle-left"></i>', '<i class="pe-7s-angle-right"></i>'],
        autoplayTimeout: 5000,
        item: 1,
        responsive: {
          0: {
            items: 1,
            autoplay: true,
          },
          576: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });

      /* Brand logo active */
      $(".brand-logo-active").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        item: 5,
        margin: 30,
        responsive: {
          0: {
            items: 2,
          },
          576: {
            items: 3,
          },
          768: {
            items: 4,
          },
          992: {
            items: 5,
          },
          1000: {
            items: 5,
          },
        },
      });

      /* Brand logo active */
      $(".brand-logo-active-2").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        item: 4,
        margin: 45,
        responsive: {
          0: {
            items: 1,
          },
          576: {
            items: 3,
          },
          768: {
            items: 3,
          },
          992: {
            items: 4,
          },
          1000: {
            items: 4,
          },
        },
      });

      /* Related product active */
      $(".related-product-active").owlCarousel({
        loop: true,
        nav: false,
        autoplay: false,
        autoplayTimeout: 5000,
        item: 4,
        margin: 30,
        responsive: {
          0: {
            items: 1,
          },
          576: {
            items: 2,
          },
          768: {
            items: 2,
          },
          992: {
            items: 3,
          },
          1200: {
            items: 4,
          },
        },
      });

      /*--- Quickview-slide-active ---*/
      $(".quickview-slide-active").owlCarousel({
        loop: true,
        navText: ["<i class='fa fa-angle-left'></i>", "<i class='fa fa-angle-right'></i>"],
        margin: 15,
        smartSpeed: 1000,
        nav: true,
        dots: false,
        responsive: {
          0: {
            items: 3,
            autoplay: true,
            smartSpeed: 300,
          },
          576: {
            items: 3,
          },
          768: {
            items: 3,
          },
          1000: {
            items: 3,
          },
        },
      });

      $(".quickview-slide-active a").on("click", function() {
        $(".quickview-slide-active a").removeClass("active");
      });

      /*----------------------------
    	Cart Plus Minus Button
    ------------------------------ */
      var CartPlusMinus = $(".cart-plus-minus");
      CartPlusMinus.prepend('<div class="dec qtybutton">-</div>');
      CartPlusMinus.append('<div class="inc qtybutton">+</div>');
      $(".qtybutton").on("click", function() {
        var $button = $(this);
        var oldValue = $button
          .parent()
          .find("input")
          .val();
        if ($button.text() === "+") {
          var newVal = parseFloat(oldValue) + 1;
        } else {
          // Don't allow decrementing below zero
          if (oldValue > 0) {
            newVal = parseFloat(oldValue) - 1;
          } else {
            newVal = 1;
          }
        }
        $button
          .parent()
          .find("input")
          .val(newVal);
      });

      /*--
    Menu Stick
    -----------------------------------*/
      var header = $(".sticky-bar");
      var win = $(window);
      win.on("scroll", function() {
        var scroll = win.scrollTop();
        if (scroll < 200) {
          header.removeClass("stick");
        } else {
          header.addClass("stick");
        }
      });

      /* jQuery MeanMenu */
      $("#mobile-menu-active").meanmenu({
        meanScreenWidth: "991",
        meanMenuContainer: ".mobile-menu-area .mobile-menu",
      });

      /*-----------------------------------
        Scroll zoom
    -------------------------------------- */
      // eslint-disable-next-line no-undef
      window.sr = ScrollReveal({
        duration: 800,
        reset: false,
      });
      // eslint-disable-next-line no-undef
      sr.reveal(".scroll-zoom");

      /*-----------------------
        Shop filter active
    ------------------------- */
      $(".filter-active a").on("click", function(e) {
        e.preventDefault();
        $(".product-filter-wrapper").slideToggle();
      });

      /*---------------------
        Price slider
    --------------------- */
      var sliderrange = $("#slider-range");
      var amountprice = $("#amount");
      $(function() {
        sliderrange.slider({
          range: true,
          min: 16,
          max: 400,
          values: [0, 300],
          slide: function(event, ui) {
            amountprice.val("$" + ui.values[0] + " - $" + ui.values[1]);
          },
        });
        amountprice.val("$" + sliderrange.slider("values", 0) + " - $" + sliderrange.slider("values", 1));
      });

      /* Language dropdown */
      $(".language-style a").on("click", function(e) {
        e.preventDefault();
        $(this)
          .parent()
          .find(".lang-car-dropdown")
          .slideToggle("medium");
      });

      /* use style dropdown */
      $(".use-style a").on("click", function(e) {
        e.preventDefault();
        $(this)
          .parent()
          .find(".lang-car-dropdown")
          .slideToggle("medium");
      });

      /*=========================
		Toggle Ativation
	===========================*/
      function itemToggler() {
        $(".toggle-item-active")
          .slice(0, 8)
          .show();
        $(".item-wrapper")
          .find(".loadMore")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper")
              .find(".toggle-item-active:hidden")
              .slice(0, 4)
              .slideDown();
            if ($(".toggle-item-active:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn")
                .fadeOut("slow");
            }
          });
      }
      itemToggler();

      function itemToggler2() {
        $(".toggle-item-active2")
          .slice(0, 8)
          .show();
        $(".item-wrapper2")
          .find(".loadMore2")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper2")
              .find(".toggle-item-active2:hidden")
              .slice(0, 4)
              .slideDown();
            if ($(".toggle-item-active2:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn2")
                .fadeOut("slow");
            }
          });
      }
      itemToggler2();

      function itemToggler3() {
        $(".toggle-item-active3")
          .slice(0, 8)
          .show();
        $(".item-wrapper3")
          .find(".loadMore3")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper3")
              .find(".toggle-item-active3:hidden")
              .slice(0, 4)
              .slideDown();
            if ($(".toggle-item-active3:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn3")
                .fadeOut("slow");
            }
          });
      }
      itemToggler3();

      /*--------------------------
        ScrollUp
    ---------------------------- */
      $.scrollUp({
        scrollText: '<i class="fa fa-angle-double-up"></i>',
        easingType: "linear",
        scrollSpeed: 900,
        animation: "fade",
      });

      /*--------------------------
        Isotope
    ---------------------------- */

      $(".grid").imagesLoaded(function() {
        // init Isotope
        $(".grid").isotope({
          itemSelector: ".grid-item",
          percentPosition: true,
          layoutMode: "masonry",
          masonry: {
            // use outer width of grid-sizer for columnWidth
            columnWidth: ".grid-sizer",
          },
        });
      });

      /*--- Clickable menu active ----*/
      // eslint-disable-next-line no-unused-vars
      const slinky = $("#menu").slinky();

      /*====== sidebarCart ======*/
      function sidebarMainmenu() {
        var menuTrigger = $(".clickable-mainmenu-active"),
          endTrigger = $("button.clickable-mainmenu-close"),
          container = $(".clickable-mainmenu");
        menuTrigger.on("click", function(e) {
          e.preventDefault();
          container.addClass("inside");
        });
        endTrigger.on("click", function() {
          container.removeClass("inside");
        });
      }
      sidebarMainmenu();

      /*=========================
		Toggle Ativation
	===========================*/
      function itemToggler4() {
        $(".toggle-item-active4")
          .slice(0, 6)
          .show();
        $(".item-wrapper4")
          .find(".loadMore4")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper4")
              .find(".toggle-item-active4:hidden")
              .slice(0, 3)
              .slideDown();
            if ($(".toggle-item-active4:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn4")
                .fadeOut("slow");
            }
          });
      }
      itemToggler4();

      function itemToggler5() {
        $(".toggle-item-active5")
          .slice(0, 6)
          .show();
        $(".item-wrapper5")
          .find(".loadMore5")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper5")
              .find(".toggle-item-active5:hidden")
              .slice(0, 3)
              .slideDown();
            if ($(".toggle-item-active5:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn5")
                .fadeOut("slow");
            }
          });
      }
      itemToggler5();

      function itemToggler6() {
        $(".toggle-item-active6")
          .slice(0, 6)
          .show();
        $(".item-wrapper6")
          .find(".loadMore6")
          .on("click", function(e) {
            e.preventDefault();
            $(this)
              .parents(".item-wrapper6")
              .find(".toggle-item-active6:hidden")
              .slice(0, 3)
              .slideDown();
            if ($(".toggle-item-active6:hidden").length == 0) {
              $(this)
                .parent(".toggle-btn6")
                .fadeOut("slow");
            }
          });
      }
      itemToggler6();

      /*---------------------
        Countdown
      --------------------- */
      $("[data-countdown]").each(function() {
        var $this = $(this),
          finalDate = $(this).data("countdown");
        $this.countdown(finalDate, function(event) {
          $this.html(
            event.strftime(
              '<span class="cdown day">%-D <p>Days</p></span> <span class="cdown hour">%-H <p>Hours</p></span> <span class="cdown minutes">%M <p>Minutes</p></span class="cdown second"> <span>%S <p>Second</p></span>'
            )
          );
        });
      });

      /*--------------------------
        Product Zoom
	---------------------------- */
      $(".zoompro").elevateZoom({
        gallery: "gallery",
        galleryActiveClass: "active",
        zoomWindowWidth: 300,
        zoomWindowHeight: 100,
        scrollZoom: false,
        zoomType: "inner",
        cursor: "crosshair",
      });

      /*---------------------
        Product dec slider
    --------------------- */
      $(".product-dec-slider-2").slick({
        infinite: true,
        slidesToShow: 4,
        vertical: true,
        slidesToScroll: 1,
        centerPadding: "60px",
        prevArrow: '<span class="product-dec-icon product-dec-prev"><i class="fa fa-angle-up"></i></span>',
        nextArrow: '<span class="product-dec-icon product-dec-next"><i class="fa fa-angle-down"></i></span>',
        responsive: [
          {
            breakpoint: 992,
            settings: {
              slidesToShow: 4,
              slidesToScroll: 1,
            },
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 1,
            },
          },
          {
            breakpoint: 479,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 1,
            },
          },
        ],
      });

      /*---------------------
        Video popup
    --------------------- */
      $(".video-popup").magnificPopup({
        type: "iframe",
        mainClass: "mfp-fade",
        removalDelay: 160,
        preloader: false,
        zoom: {
          enabled: true,
        },
      });

      /*---------------------
        Sidebar active
    --------------------- */
      $(".sidebar-active").stickySidebar({
        topSpacing: 80,
        bottomSpacing: 30,
        minWidth: 767,
      });

      /* Product details slider */
      $(".product-details-slider-active").owlCarousel({
        loop: true,
        nav: true,
        autoplay: false,
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        navText: ['<i class="fa fa-chevron-left"></i>', '<i class="fa fa-chevron-right"></i>'],
        item: 3,
        margin: 30,
        responsive: {
          0: {
            items: 1,
          },
          768: {
            items: 3,
          },
          1000: {
            items: 3,
          },
        },
      });

      /*--
    Magnific Popup
    ------------------------*/
      $(".img-popup").magnificPopup({
        type: "image",
        gallery: {
          enabled: true,
        },
      });

      /*-------------------------
    Create an account toggle
    --------------------------*/
      $(".checkout-toggle2").on("click", function() {
        $(".open-toggle2").slideToggle(1000);
      });

      $(".checkout-toggle").on("click", function() {
        $(".open-toggle").slideToggle(1000);
      });

      /*---- CounterUp ----*/
      $(".count").counterUp({
        delay: 10,
        time: 1000,
      });

      /* Blog img slide active */
      $(".blog-img-slide").owlCarousel({
        loop: true,
        nav: true,
        dots: false,
        autoplay: false,
        autoplayTimeout: 5000,
        animateOut: "fadeOut",
        animateIn: "fadeIn",
        navText: ['<i class="fa fa-angle-left"></i>', '<i class="fa fa-angle-right"></i>'],
        item: 1,
        margin: 30,
        responsive: {
          0: {
            items: 1,
          },
          768: {
            items: 1,
          },
          1000: {
            items: 1,
          },
        },
      });

      /*====== fullpage slider active ======*/

      $("#fullpage").fullpage({
        sectionSelector: ".flone-fp-section",
        slideSelector: ".flone-fp-slide",
        navigation: true,
        responsiveWidth: 575,
      });

      /*------ Wow Active ----*/
      // eslint-disable-next-line no-undef
      new WOW().init();
      // eslint-disable-next-line no-undef
    })(jQuery);
  },
  methods: {
    getUserId: function() {
      return localStorage.getItem("user.id");
    },
  },
  isLoggedIn: function() {
    if (localStorage.getItem("jwt")) {
      return true;
    } else {
      return false;
    }
  },
  isAdmin: function() {
    if (localStorage.getItem("user_admin")) {
      return true;
    } else {
      return false;
    }
  },
  // here goes is Admin when its fixed **rememeber to add ${} to interpolate also call with $parent.
};
</script>
