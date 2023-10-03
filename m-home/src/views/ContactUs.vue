<template>
    <section id="about-us">

        <h1 class="main-heading">Send us a mail</h1>

    </section>
    <div class="container">
        <p class="mt-10">Welcome to Mercury Home, where impeccable designs meet your unique sense of style. We are your
            premier destination for exquisite home designs and curated decorations that transform houses into personalized
            havens. With an unwavering commitment to quality and an eye for innovation, Mercury Home is owned and led by the
            visionary entrepreneur, Kagiso Monageng.</p>


        <div class="grid grid-cols-3">
            <div class="col">
                <h2 class="mb-0">Contact us</h2>
                <p class="mb-0">Email: <strong>kagisoboasmonageng@gmail.com</strong></p>
                <p>Tel: <strong>(+27) 08 876 8734</strong></p>
            </div>
            <div class="col">
                <h2 class="mb-0">Find us</h2>
                <p class="mb-0">15 Fest Street</p>
                <p class="mb-0">Pretzel North</p>
                <p class="mb-0">Gauteng</p>
            </div>
        </div>

        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3582.9133290090404!2d28.071507375158042!3d-26.1017477598087!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1e9572d3cf20bd4d%3A0x4ca4e1dad16cbb19!2sPinmill%20Farm!5e0!3m2!1sen!2sza!4v1696366044264!5m2!1sen!2sza" width="100%" height="600" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>




        <!-- <p>Tel: <strong>(+27) 08 876 8734</strong></p> -->

    </div>
</template>
 
<style>
section#about-us {
    background-image: url(../assets/images/about-cover.jpg);
    min-height: 50vh !important;
    display: flex;
    justify-content: center;
    place-items: center;
    background-attachment: fixed;
}

.main-heading {
    font-size: 40px;
    font-weight: 600;
    color: #fff;
    position: relative;
}

.main-heading::after {
    content: '';
    position: absolute;
    height: 40%;
    aspect-ratio: 1/1;
    left: -10px;
    top: 0;
    backdrop-filter: blur(20px);
    border: 1px solid #fff;
}

.main-heading::before {
    content: '';
    position: absolute;
    width: 30%;
    height: 50%;
    right: -50px;
    top: 20px;
    border: 1px solid #fff;
    backdrop-filter: blur(20px);

}


.gradient-text {
    background: #12c2e9;
    background: linear-gradient(to right, #12c2e9 0%, #C471ED 50%, #F64F59 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
</style>
<script>
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger);

gsap.to(".main-heading", {
    opacity: 0, scrollTrigger: {
        trigger: ".main-heading",
        start: "top 10%",
        scrub: true,
    }
})


</script>
 