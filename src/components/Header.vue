<template>
  <div class="bg-pink">
    <div class="w-100 fl dn-l ph2  pv3 bg-pink ">
      <div class="w-25 pt2 fl pointer" @click="toggleMenu">
        <i class="fa f4 pl2 pt3 fa-bars"></i>
      </div>

      <div class="w-50 pr2 tc fl ">
        <img src="@/assets/abyalogo.png"  class="h3" />
      </div>

      <div class="w-25 pt2 fl  ">
        <i class="fa f4 pt3 ph3 fa-search" aria-hidden="true"></i>
        <i class="fa f4 pt3 fa-shopping-basket" aria-hidden="true"></i> 
      </div>
    </div>

    <header class="bg-pink fl w-100 dn dib-l black-80 tc pv3 avenir">
      <img src="@/assets/abyalogo.png"  class="h3" /> 
      <nav class="bt bb b--purple tc mw7 center mt2">
        <a class="f6 f5-l link bg-animate black-80 hover-bg-purple dib pa3 ph4-l" href="/">Home</a>
        <a class="f6 f5-l link bg-animate black-80 hover-bg-light-purple dib pa3 ph4-l" href="/shop">Shop</a>
        <a class="f6 f5-l link bg-animate black-80 hover-bg-light-purple dib pa3 ph4-l" href="/blog">Blog</a>
        <a class="f6 f5-l link bg-animate black-80 hover-bg-light-purple dib pa3 ph4-l" href="/cart">Cart</a>
        <router-link class="f6 f5-l link bg-animate black-80 hover-bg-light-purple dib pa3 ph4-l" to="/about">Contact</router-link>
      </nav>
    </header>


    <div class=" cf w-100 bg-black">
        <div class="top-0 left-0 vh-100 fl w-100 fixed bg-black-30 absolute z-max dn" :class="{'slideInLeft':lShow, 'slideOutLeft':!lShow}"> 
          <div class="fl w-100 ">
            <div class="fl w-100 pointer "  @click="toggleMenu">    
              <div class="ph2 w-70 center pt3 fl vh-100 z-max fw5 bg-light-pink dn-l dark-gray">
                <div class="fl w-100">
                  <i class="fal fa-times-circle"></i>
                  <div class="b pl2 pv3 f5 f6-m">
                      <input class="f6 f5-l input-reset bn fl black-80 bg-white pa3 lh-solid w-100 br-pill " placeholder="Search..." type="text" name="search" value="" id="search">
                  </div>
                </div>
                <div class="fl w-100">
                  <div class="b pl2 pv4 f5 f6-m">
                      > Cookies
                  </div>
                </div>
                <div class="fl w-100">
                  <div class="b pl2 pb4 f5 f6-m">
                      > Blondies
                  </div>
                </div>
                <div class="fl w-100">
                  <div class="b pl2 pb4 f5 f6-m">
                      > Brownies
                  </div>
                </div>
                <div class="fl w-100">
                  <div class="b pl2 pb4 f5 f6-m">
                      > Banana Bread
                  </div>
                </div>
                <div class="fl w-100">
                  <div class=" pl2 pb4 f5 f6-m">
                      > Build a box
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="fl w-100 ">
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      lShow:false,
        slideOut:"dn", 
        height:0, padtop:0,
    }},
    created () { 
        //style="height:calc(100vh - 6rem)"
        this.height = window.innerHeight - 64 + 'px'
        // this.padtop = (window.outerHeight-window.innerHeight)+64 + 'px'
        this.padtop = 64+'px'
    },
  methods: {
  toggleMenu() {
      this.lShow = !this.lShow
      // document.getElementsByTagName("html")[0].classList.toggle('overflow-hidden');
  },
  }
}
</script>
