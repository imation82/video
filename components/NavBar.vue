<template>
    <section id="topmenu">
        <nav class="menu navbar navbar-expand-lg">
            <div class="container">
                <a href="#topmenu" v-smooth-scroll>
                    <img src="~assets/images/logo.png" alt="Logo">
                </a>
                <div class="menu__desktop d-none d-lg-block">
                    <ul class="menu__list navbar-nav ms-auto">
                        <li v-for="(menus, i) in menu" :key="i" class="nav-item">
                            <a :href="menus.link" class="nav-link" v-smooth-scroll>{{ menus.name }}</a>
                        </li>
                    </ul>                
                </div>          
                <div @click="isShow = !isShow" class="menu__mobile d-block d-lg-none">
                    <div></div>
                    <div></div>
                    <div></div>
                </div>
                <transition name="slide-fade">
                <div v-if="isShow" class="menu__mobile--show">
                    <div class="d-flex justify-content-between">
                        <div>
                            <h3>VideoTC</h3>
                            <ul class="navbar-nav">
                                <li v-for="(menus, i) in menu" :key="i" class="nav-item">
                                    <a @click="isShow = false" :href="menus.link" class="nav-link d-flex align-items-center" v-smooth-scroll>
                                        <img :src="menus.menu" :alt="menus.alt" class="me-4">{{ menus.name }}
                                    </a>
                                </li>                          
                            </ul>
                        </div>
                        <div>
                            <img @click="close" src="~assets/svg/cross.svg" alt="Close">
                        </div>
                    </div>
                </div>  
                </transition>           
            </div>               
        </nav>        
    </section>
</template>

<script>

import navHome from "~/assets/svg/home.svg";
import navFeatures from "~/assets/svg/features.svg";
import navTestimonial from "~/assets/svg/testimonial.svg";
import navAbout from "~/assets/svg/about.svg";

export default {
    data() {
        return {
            isShow:false,
            menu: [
                {
                    menu: navHome,
                    name: "Home",
                    alt: "Home",
                    link: "#topmenu"
                },
                {
                    menu: navFeatures,
                    name: "Features",
                    alt: "Features",
                    link: "#features"
                },
                {
                    menu: navTestimonial,
                    name: "Testimonial",
                    alt: "Testimonial",
                    link: "#testimonial"
                },
                {
                    menu: navAbout,
                    name: "About",
                    alt: "About",
                    link: "#about"
                }
            ]
        }
    },
    methods: {
        close() {
            this.isShow = false;
        },
    }
}

</script>