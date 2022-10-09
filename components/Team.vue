<template>
    <section id="about" class="team">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="team__headline d-block mx-auto text-center">
                        <h3>Meet our team</h3>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-3 d-none d-lg-block" v-for="(teams, i) in team" :key="i">
                    <div class="team__profile mb-4">
                        <img :src="teams.img" :alt="teams.alt" class="img-fluid d-block mx-auto w-100">
                        <div class="team__profile--content text-center">
                            <h4>{{ teams.name }}</h4>
                            <h5>{{ teams.position }}</h5>
                        </div>
                    </div>
                </div>
            </div>
            <VueSlickCarousel v-bind="slickOptions" class="d-block d-lg-none">
                <div class="col-lg-3" v-for="(teams, i) in team" :key="i">
                    <div class="team__profile mb-4">
                        <img :src="teams.img" :alt="teams.alt" class="img-fluid d-block mx-auto w-100">
                        <div class="team__profile--content text-center">
                            <h4>{{ teams.name }}</h4>
                            <h5>{{ teams.position }}</h5>
                        </div>
                    </div>
                </div>
            </VueSlickCarousel>            
        </div>
    </section>
    
</template>

<script>

import VueSlickCarousel from 'vue-slick-carousel';    

import team01 from "~/assets/images/team/nicholas.jpg";
import team02 from "~/assets/images/team/jessica.jpg";
import team03 from "~/assets/images/team/samantha.jpg";
import team04 from "~/assets/images/team/nicole.jpg";
import team05 from "~/assets/images/team/mitchell.jpg";
import team06 from "~/assets/images/team/dane.jpg";
import team07 from "~/assets/images/team/hasan.jpg";
import team08 from "~/assets/images/team/julia.jpg";
import team09 from "~/assets/images/team/ariful.jpg";
import team10 from "~/assets/images/team/rahima.jpg";
import team11 from "~/assets/images/team/ward.jpg";


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
              breakpoint: 768,
              settings: {
                slidesToShow: 3,
              },
            },
            {
              breakpoint: 767,
              settings: {
                slidesToShow: 2,
              },
            }                                      
        ]           
    },            
            team: [
                {
                    img: team01,
                    name: "Nicholas P",
                    alt: "Nicholas",
                    position: "Founder CEO"
                },
                {
                    img: team02,
                    name: "Jessica K",
                    alt: "Jessica",
                    position: "Product Manager"
                },                
                {
                    img: team03,
                    name: "Samantha P",
                    alt: "Samantha",
                    position: "Founder"
                },
                {
                    img: team04,
                    name: "Nicole P",
                    alt: "Nicole",
                    position: "Co-Founder"
                },
                {
                    img: team05,
                    name: "Mitchell N",
                    alt: "Mitchell",
                    position: "Co-Founder"
                },
                {
                    img: team06,
                    name: "Dane B",
                    alt: "Dane",
                    position: "VP Project Manager"
                },
                {
                    img: team07,
                    name: "Hasan H",
                    alt: "Hasan",
                    position: "Advisor"
                },
                {
                    img: team08,
                    name: "Julia M",
                    alt: "Julia",
                    position: "Consultant"
                },
                {
                    img: team09,
                    name: "Ariful H",
                    alt: "Ariful",
                    position: "UI/UX Designer"
                },
                {
                    img: team10,
                    name: "Rahima S",
                    alt: "Rahima",
                    position: "Programmer"
                },
                {
                    img: team11,
                    name: "Ward G",
                    alt: "Ward",
                    position: "Programmer"
                }                                                      
            ]
        }
    },
}
</script>