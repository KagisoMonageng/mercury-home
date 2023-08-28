<template>
   <section id="about-us">

    <h1 class="main-heading">About Us</h1>

   </section> 
   <div class="container">
    <p class="mt-10">Welcome to Mercury Home, where impeccable designs meet your unique sense of style. We are your premier destination for exquisite home designs and curated decorations that transform houses into personalized havens. With an unwavering commitment to quality and an eye for innovation, Mercury Home is owned and led by the visionary entrepreneur, Kagiso Monageng.</p>

    <h2>Vision</h2>
    <p>At Mercury Home, we envision a world where every living space reflects the individuality and aspirations of its occupants. We believe that the right design and décor can elevate everyday living into an art form, fostering a harmonious blend of aesthetics, comfort, and functionality.</p>
    <h2>Meet the Founder<span>Kagiso Monageng</span></h2>
    <p>Mercury Home was brought to life by the creative genius of Kagiso Monageng. With a passion for design and an innate understanding of the impact of aesthetics on our lives, Kagiso embarked on a journey to create a brand that resonates with those who seek to curate their spaces with unparalleled beauty and elegance. Kagiso's commitment to excellence and his unique design sensibilities are the driving forces behind Mercury Home's success.</p>

    <h2>Our Distinctive Approach</h2>
    <p>What sets Mercury Home apart is our unwavering dedication to crafting designs that are not just visually appealing, but also deeply personal. We understand that your home is an extension of your personality, and our team of talented designers strives to translate your dreams and ideas into stunning, tangible realities. Each piece in our collection is handpicked to seamlessly blend contemporary trends with timeless classics, ensuring that your space remains a testament to your discerning taste for years to come.</p>
   </div>
 
</template>

<style>
section#about-us{
    background-image: url(../assets/images/about-cover.jpg);
    min-height: 50vh !important;
    display: flex;
    justify-content: center;
    place-items: center;
    background-attachment: fixed;
}

.main-heading{
    font-size: 40px;
    font-weight: 600;
    color: #fff;
    position: relative;
}
.main-heading::after{
    content: '';
    position: absolute;
    height: 40%;
    aspect-ratio: 1/1;
    left: -10px;
    top: 0;
    backdrop-filter: blur(20px);
    border: 1px solid #fff;
}
.main-heading::before{
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
