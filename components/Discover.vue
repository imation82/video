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

import slider01 from "~/assets/images/discover/discover-1.svg";
import slider02 from "~/assets/images/discover/discover-2.svg";
import slider03 from "~/assets/images/discover/discover-3.svg";
import slider04 from "~/assets/images/discover/discover-4.svg";
import slider05 from "~/assets/images/discover/discover-1.svg";
import slider06 from "~/assets/images/discover/discover-2.svg";

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
        draggable: false,
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
            },
            {
                slide: slider05,
                alt: "Slide 05"
            },
            {
                slide: slider06,
                alt: "Slide 06"
            }                        
        ]
    }
  }
}


</script>