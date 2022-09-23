<template>
    <nav class="menu navbar navbar-expand-lg">
        <div class="container">
            <a href="#">
                <img src="~assets/images/logo.png" alt="Logo">
            </a>
            <div class="menu__desktop d-none d-lg-block">
                <ul class="menu__list navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Testimonial</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">About us</a>
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
                            <li v-for="(mobileMenus, i) in mobileMenu" :key="i" class="nav-item">
                                <a class="nav-link d-flex align-items-center" href="#">
                                    <img :src="mobileMenus.menu" :alt="mobileMenus.alt" class="me-4">{{ mobileMenus.name }}
                                </a>
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
            mobileMenu: [
                {
                    menu: navHome,
                    name: "Home",
                    alt: "Home"
                },
                {
                    menu: navFeatures,
                    name: "Features",
                    alt: "Features"
                },
                {
                    menu: navTestimonial,
                    name: "Testimonial",
                    alt: "Testimonial"
                },
                {
                    menu: navAbout,
                    name: "About",
                    alt: "About"
                }
            ]
        }
    }
}

</script>
