<template>
    <section id="testimonial" class="testimonial">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="testimonial__headline d-block mx-auto text-center">
                        <h3>What our users says</h3>
                    </div>
                </div>
            </div>
            <VueSlickCarousel v-bind="slickOptions">
                <div v-for="(testimonials, i) in testimonial" :key="i">
                  <div class="testimonial__slider">
                    <h3 class="text-center">{{ testimonials.title }}</h3>
                    <p class="text-left">{{ testimonials.comments }}</p>
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
                </div>
            </VueSlickCarousel> 
        </div>
    </section>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';

import client from "~/assets/images/testimonial/user.png";

export default {
  components: {
    VueSlickCarousel
  },
  data() {
    return {
      slickOptions: {
        slidesToShow: 2,
        arrows: false,
        dots: true,
        adaptiveHeight: false,
        draggable: true,
        autoplay: false,
        slidesToScroll: 1,
        responsive: [
            {
              breakpoint: 1200,
              settings: {
                adaptiveHeight: true,
                slidesToShow: 2,
              },
            },            
            {
              breakpoint: 1199,
              settings: {
                adaptiveHeight: true,
                slidesToShow: 1,
              },
            },
            {
              breakpoint: 991,
              settings: {
                adaptiveHeight: true,
                slidesToShow: 1,
              },
            }                        
        ]           
      },
      testimonial: [
        {
            title: "' Amazing App for all Generations! '",
            comments: "This app is so easy to use. My 93 year-old grandmother loves to record stories from her childhood and adolescence on this app. She has no trouble using it. The videos are very easy to record and the questions are so engage. Would totally recommend this app to anyone who wants to preserve their family story!",
            name: "S.S",
            alt: "Sammypoth",
            clientImg: client,
            rating: "★★★★★"
        },
        {
            title: "' My MOM Loves This '",
            comments: "My mom used the app to tell stories about our family and the stories are so great. She told of how she met my father and its information I never knew. I now will have the information in a video. It is truly amazing. To think that I now will have her life told by her for now and forever. I used to do videos of her but they were cumbersome and not organized. This app took care of that issue. LOVE THIS APP.",
            name: "N.J",
            alt: "Nicopoth",
            clientImg: client,
            rating: "★★★★★"            
        },
        {
            title: "' This is the best app for storing video memories!! '",
            comments: "What a wonderful app for storing video memories. It engages family members to tell their stories and viewpoints about precious life events. Very easy to use even for the old generation. 5 stars.",
            name: "Cocochloe",
            alt: "Cocochooe",
            clientImg: client,
            rating: "★★★★★"            
        }                    
      ]
    }
  }
}
</script>