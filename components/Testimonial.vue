<template>
    <section class="testimonial">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="testimonial__headline d-block mx-auto text-center">
                        <h3>What our users says</h3>
                    </div>
                </div>
            </div>
            <VueSlickCarousel v-bind="slickOptions">
                <div v-for="(testimonials, i) in testimonial" :key="i" class="testimonial__slider">
                    <p class="text-center">{{ testimonials.comments }}</p>
                    <div class="testimonial__content d-flex justify-content-center">
                        <div>
                            <img :src="testimonials.clientImg" :alt="testimonials.alt"/>
                        </div>
                        <div>
                            <h4>{{ testimonials.name }}</h4>
                            <span class="testimonial__content--rating">{{ testimonials.rating }}</span>
                        </div>
                    </div>
                </div>
            </VueSlickCarousel> 
        </div>
    </section>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';

import client01 from "~/assets/images/testimonial/client-1.jpg";
import client02 from "~/assets/images/testimonial/client-2.jpg";

export default {
  components: {
    VueSlickCarousel
  },
  data() {
    return {
      slickOptions: {
        slidesToShow: 3,
        arrows: false,
        dots: true,
        adaptiveHeight: true,
        centerPadding: '0',
        draggable: false,
        responsive: [
            {
              breakpoint: 1200,
              settings: {
                slidesToShow: 3,
              },
            },            
            {
              breakpoint: 1199,
              settings: {
                slidesToShow: 2,
              },
            },
            {
              breakpoint: 991,
              settings: {
                slidesToShow: 1,
              },
            }                        
        ]           
      },
      testimonial: [
        {
            comments: "Disable wireframe mode at any time to render your project as a high-fidelity mockup.",
            name: "Daanvielen",
            alt: "Daanvielen",
            clientImg: client01,
            rating: "★★★★★"
        },
        {
            comments: "Disable wireframe mode at any time to render your project as a high-fidelity mockup.",
            name: "Thewiscokid",
            alt: "Thewiscokid",
            clientImg: client02,
            rating: "★★★★★"            
        },
        {
            comments: "Disable wireframe mode at any time to render your project as a high-fidelity mockup.",
            name: "Daanvielen",
            alt: "Daanvielen",
            clientImg: client01,
            rating: "★★★★★"            
        },
        {
            comments: "Disable wireframe mode at any time to render your project as a high-fidelity mockup.",
            name: "Thewiscokid",
            alt: "Thewiscokid",
            clientImg: client02,
            rating: "★★★★★"            
        }                        
      ]
    }
  }
}
</script>