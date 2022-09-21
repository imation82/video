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
            <div class="row">
                <div class="col-lg-11 offset-lg-1">
                    <VueSlickCarousel v-bind="slickOptions">
                        <div v-for="(testimonials, i) in testimonial" :key="i" class="testimonial__slider">
                            <p class="text-center">{{ testimonials.comments }}</p>
                            <div class="testimonial__content d-flex justify-content-center align-items-center">
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
            </div>
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
        dots: true
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