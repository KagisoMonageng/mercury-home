<template>
  <div id="smooth-wrapper">
    <div id="smooth-content">
      <section id="home" class="relative">
        <div class="container">
          <!-- <h1 class="main-hero">Welcome to Mercury Home</h1>
      <h3></h3> -->

          <div class="wrap w-full text-center text-white">
            <h1><span>Welcome to</span>Mercury Home</h1>
            <p class="my-2">Where Elegance Meets Comfort!</p>

            <p class="w-1/2 mx-auto mt-8">At Mercury Home, we believe that your home should be a sanctuary, a place where
              you
              can truly express yourself and find solace in the beauty of your surroundings. Our passion lies in helping
              you
              transform your living spaces into captivating and cozy havens that reflect your unique style and
              personality.
            </p>

            <RouterLink to="/about" class="link mx-auto">Read more <i class="fi fi-rr-angle-circle-right"></i>
            </RouterLink>
          </div>
        </div>
        <div class="scroller w-full flex justify-center absolute bottom-4 text-2xl text-center text-white">
          <i class="fi fi-rr-mouse scroll-attention" id="scroller"></i>
        </div>
      </section>
      <article class="my-12">
        <div class="container">

          <div class="flex flex-col lg:flex-row gap-12 justify-center px-3">
            <div class="col w-full lg:w-1/3">
              <div class="graphic">
                <div class="content">
                  <i class="fi fi-rr-house-blank"></i>
                  <p class="title">Exquisite</p>
                  <p class="short-copy">
                    Discover curated elegance for your space at Mercury Home. Elevate every corner with our exquisite
                    decor
                    pieces.
                  </p>
                </div>

              </div>
            </div>
            <div class="col w-full lg:w-1/3 pt-5">
              <p class="font-light">Explore our curated collection of exquisite home decor and furnishings, carefully
                selected
                to elevate your
                interiors to new heights of sophistication. Whether you're searching for timeless classics, modern
                minimalism,
                or
                eclectic statement pieces, we've got you covered.</p>
            </div>


          </div>

          <div class="flex flex-col lg:flex-row-reverse gap-12 justify-center px-3 mt-12">
            <div class="col w-full lg:w-1/3">
              <div class="graphic">
                <div class="content">
                  <i class="fi fi-rr-bed-alt"></i>
                  <p class="title">Luxurious</p>
                  <p class="short-copy">
                    Experience the allure of luxury at Mercury Home, where opulent treasures await to adorn your living
                    spaces
                    with sophistication and refinement.
                  </p>
                </div>

              </div>
            </div>
            <div class="col w-full lg:w-1/3 pt-5">
              <p class="font-light">From luxurious furniture that beckons you to unwind, to enchanting decor accents that
                breathe life into your
                spaces, Mercury Home offers a diverse array of choices to inspire your creativity and ignite your
                imagination.
              </p>
            </div>


          </div>
          <p class="font-light mt-12 lg:w-3/4 text-center mx-auto">Join us on this journey of crafting homes that resonate
            with your soul. With Mercury Home, your dream home is
            just a click away. Explore our collections today and start creating the space you've always envisioned!</p>
        </div>
      </article>
      <footer class="graphic">
        <div class="content">
          <p class="title">Subscribe to our Newsletter</p>
          <p class="short-copy">Stay inspired, subscribe today!</p>
          <form action="">
            <div class="flex flex-col lg:flex-row gap-6 place-items-center">
              <div class="form-group flex flex-col place-items-start gap-1">
                <input type="text" class="input main-input" placeholder="Enter your email">
              </div>
              <button class="btn form-btn">Subscribe</button>


            </div>
          </form>

        </div>

      </footer>
    </div>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router';
import { gsap } from 'gsap';
// import { ScrollSmoother} from 'gsap/ScrollSmoother'
import { ScrollTrigger} from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger);
</script>

<style lang="scss" scoped>.wrap {
  min-height: 50vh;
}</style>

