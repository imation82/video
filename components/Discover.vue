<template>
    <section class="discover">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="discover__headline d-block mx-auto text-center">
                        <h3>Discover some demo</h3>
                    </div>
                </div>
            </div>
            <div class="discover__slider">
                <VueSlickCarousel v-bind="slickOptions">
                    <div v-for="(discoverSliders, i) in discoverSlider" :key="i">
                        <img :src="discoverSliders.slide" :alt="discoverSliders.alt" class="d-block mx-auto">                    
                    </div>
                </VueSlickCarousel>       
            </div>         
        </div>
    </section>
</template>

<script>

import VueSlickCarousel from 'vue-slick-carousel';

import slider01 from "~/assets/images/discover/discover-1.png";
import slider02 from "~/assets/images/discover/discover-2.png";
import slider03 from "~/assets/images/discover/discover-3.png";
import slider04 from "~/assets/images/discover/discover-4.png";

export default {
  components: {
    VueSlickCarousel
  },
  data () {
    return {
      slickOptions: {
        slidesToShow: 3,
        arrows: false,
        dots: true,
        draggable: true,
        centerMode: true,
        autoplay: false,
        slidesToScrol: 1,
        centerPadding: "0px",
        responsive: [         
            {
              breakpoint: 1199,
              settings: {
                slidesToShow: 3,
                centerMode: true,
                centerPadding: "0px",
              },
            },
            {
              breakpoint: 1023,
              settings: {
                slidesToShow: 1,                
                centerMode: true,
                centerPadding: "0px"
              },
            }                        
        ]          
      },        
        discoverSlider: [
            {
                slide: slider01,
                alt: "Slide 01"
            },
            {
                slide: slider02,
                alt: "Slide 02"
            },
            {
                slide: slider03,
                alt: "Slide 03"
            },
            {
                slide: slider04,
                alt: "Slide 04"
            }                     
        ]
    }
  }
}


</script>