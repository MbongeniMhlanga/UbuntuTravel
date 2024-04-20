<template>
    <NuxtLink to="/"> Home </NuxtLink>
    <div class="container py-5">
        <h1 class="mb-4">About Ubuntu Travel</h1>
        <!----<h4> Travel Made Easy</h4>-->
        <div class="row">
            <div class="col-mod-6">
                <h3> ✈️ Welcome to our travel App 🌍</h3>
                <p class="lead">Your one-stop destination for all your travel needs.</p>
                <p>
                    Our travel app makes it easy to plan trips, book flights, reserve accommodation, and much more-all
                    from one convenient location. We aim to simplify your travel planning process with a user-friendly
                    interface and powerful features.
                </p>
                <p>Join us and start exploring the world with ease and comfort.</p>
            </div>

            <div class="col md-6">
                <div id="carouselExample" class="carousel slide">
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img height="300px" src="`assets/about1.jpg`" alt="image">
                        </div>
                        <div class="carousel-item">
                            <img height="300px" src="`assets/about2.jpg`" alt="image">
                        </div>
                        <div class="carousel-item">
                            <img height="300px" src="`assets/about3.jpg`" alt="image">
                        </div>
                        <div class="carousel-item">
                            <img src="`assets/about4.jpg`" alt="image">
                        </div>
                    </div>
                    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample"
                        data-bs-slide="prev">
                        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Previous</span>
                    </button>
                    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample"
                        data-bs-slide="next">
                        <span class="carousel-control-next-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Next</span>
                    </button>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

export default {
    name: 'App',
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data() {
        return {
            images: ['/assets/about1.jpg', '/assets/about2.jpg', '/assets/about3.jpg']
        };
    }
}
</script>

<style>
    img {
        width: 80%;
        max-height: 60%;
        clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
    }
</style>