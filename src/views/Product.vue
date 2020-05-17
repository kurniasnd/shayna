<template>
  <div class="product">
    <Header />
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12 text-left">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="gambar_default" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :items="3" :dots="false" :nav="false" :autoplay="true">
                                    <div class="pt" @click="chengeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : '' ">
                                        <img src="img/mickey1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="chengeImage(thumbs[1])" :class="thumbs[1] == gambar_default ? 'active' : '' ">
                                        <img src="img/mickey2.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="chengeImage(thumbs[2])" :class="thumbs[2] == gambar_default ? 'active' : '' ">
                                        <img src="img/mickey3.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="chengeImage(thumbs[3])" :class="thumbs[3] == gambar_default ? 'active' : '' ">
                                        <img src="img/mickey4.jpg" alt="" />
                                    </div>

                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Pariwisata Bali merupakan salah satu tujuan wisata yang sudah tidak diragukan lagi oleh wisatawan asing maupun wisatawan domestik.
                                    </p>
                                    <p> 
                                        Pariwisata Bali sudah menjadi tujuan wisata dunia yang terkenal di seluruh manca negara. 
                                        Hal Ini terbukti bahwa kunjungan wisatawan asing maupun wisatawan domestik ke Bali dari tahun ke tahun semakin meningkat. 
                                        Namun tidak hanya kunjungan wisatawan untuk berlibur saja yang menyebabkan faktor perkembangan kunjungan wisatawan ke Bali meningkat, akan tetapi dengan sering diadakannya acara atau event international di Bali juga salah satu faktor perkembangan peningkatan kunjungan tersebut.
                                    </p>
                                    <h4>Rp.1.999.000</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart"><a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a></router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    <RelatedProduct />
    <Footer />
    
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import RelatedProduct from '@/components/RelatedProduct.vue'; 
import Footer from '@/components/Footer.vue';

import carousel from "vue-owl-carousel";

export default {
  name: 'product',
  components: {
    Header,
    RelatedProduct,
    Footer,
    carousel
  },
  data(){
      return{
          gambar_default: "img/mickey1.jpg",
          thumbs:[
              "img/mickey1.jpg",
              "img/mickey2.jpg",
              "img/mickey3.jpg",
              "img/mickey4.jpg"
          ]
      }
  },
  methods: {
      chengeImage(urlImage){
          this.gambar_default = urlImage;
      }
  }
};
</script>

<style scoped>
.product-thumbs .pt {
    margin-right: 10px;
}

</style>
