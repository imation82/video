<template>
    <nav class="menu navbar navbar-expand-lg">
        <div class="container">
            <a href="#">
                <img src="~assets/images/logo.png" alt="Logo">
            </a>
            <div class="menu__desktop d-none d-lg-block">
                <ul class="menu__list navbar-nav ms-auto">
                    <li v-for="(menus, i) in menu" :key="i" class="nav-item">
                        <nuxt-link class="nav-link" :to="menus.link">{{ menus.name }}</nuxt-link>
                    </li>
                </ul>                
            </div>          
            <div @click="isShow = true" class="menu__mobile d-block d-lg-none">
                <div></div>
                <div></div>
                <div></div>
            </div>
            <div v-show="isShow" class="menu__mobile--show">
                <div class="d-flex justify-content-between">
                    <div>
                        <h3>VideoTC</h3>
                        <ul class="navbar-nav">
                            <li v-for="(menus, i) in menu" :key="i" class="nav-item">
                                <nuxt-link class="nav-link d-flex align-items-center" :to="menus.link">
                                    <img :src="menus.menu" :alt="menus.alt" class="me-4">{{ menus.name }}
                                </nuxt-link>
                            </li>                          
                        </ul>
                    </div>
                    <div>
                        <img src="~assets/svg/cross.svg" alt="Close">
                    </div>
                </div>
            </div>             
        </div>               
    </nav>
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
                    link: "/"
                },
                {
                    menu: navFeatures,
                    name: "Features",
                    alt: "Features",
                    link: "/"
                },
                {
                    menu: navTestimonial,
                    name: "Testimonial",
                    alt: "Testimonial",
                    link: "/"
                },
                {
                    menu: navAbout,
                    name: "About",
                    alt: "About",
                    link: "/"
                }
            ]
        }
    }
}

</script>
