<script>
import logo from '@/assets/images/logo.svg?url'
import logoDark from '@/assets/images/logo-dark.svg?url'
import imgHeader from '@/assets/images/illustration-1.svg?url'
import imgMain from '@/assets/images/illustration-2.svg?url'
import iconQuotes from '@/assets/images/icon-quotes.svg?url'
import iconArrow from '@/assets/images/icon-arrow.svg?component'
import imgAvatar from '@/assets/images/avatar-testimonial.jpg'
import iconPhone from '@/assets/images/icon-phone.svg?component'
import iconEmail from '@/assets/images/icon-email.svg?component'

import BtnNetwork from './components/BtnNetwork.vue'
import TextContent from './components/FooterContent.vue'
import curveMobile from '@/assets/images/bg-curve-mobile.svg?url'
import curveDesktop from '@/assets/images/bg-curve-desktop.svg?url'

export default {
  data() {
    return {
      logo,
      logoDark,
      imgHeader,
      imgMain,
      iconQuotes,
      imgAvatar,
      curveMobile,
      curveDesktop,
      rgxEmail: new RegExp(/^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/),
      emailOne: '',
      emailTwo: '',
      isValidOne: true,
      isValidTwo: true,
    }
  },
  components: {
    BtnNetwork,
    TextContent,
    // SVG's
    iconArrow,
    iconPhone,
    iconEmail,
  },
  methods: {
    checkEmailOne() {
      if (this.rgxEmail.test(this.emailOne)) {
        this.isValidOne = true;
        this.emailOne = '';
      } else {
        this.isValidOne = false;
      }
    },
    checkEmailTwo() {
      if (this.rgxEmail.test(this.emailTwo)) {
        this.isValidTwo = true;
        this.emailTwo = '';
      } else {
        this.isValidTwo = false;
      }
    },
    validState(validBool) {
      return validBool ? '' : 'border-neo-red';
    },
  }
}
</script>
<template>
  <header class=" flex flex-col gap-[98px] dsk:gap-[78px] mx-6 dsk:mx-20 mt-6 dsk:mt-[65px]">
    <nav class=" flex justify-between items-center">
      <img class=" w-[80px] dsk:w-[166px]" :src="logo" alt="logo">
      <div
        class=" flex justify-between w-[167px] dsk:w-[271px] text-neo-dark-blue text-[12px] dsk:text-[16px] leading-[14px] dsk:leading-[19px] font-raleway font-medium">
        <TextContent content="Features" />
        <TextContent content="Team" />
        <TextContent content="Sign In" />
      </div>
    </nav>
    <div class=" flex flex-col dsk:flex-row-reverse dsk:justify-between items-center gap-10 dsk:gap-[13px]">
      <img class=" w-[304px] dsk:w-[640px]" :src="imgHeader" alt="imgHeader">
      <div class=" flex flex-col gap-8 dsk:gap-[25px] dsk:w-[627px]">
        <div
          class=" flex flex-col items-center dsk:items-start gap-6 dsk:gap-[15px] text-center dsk:text-left text-neo-dark-blue font-open-sans">
          <h1 class=" w-[320px] dsk:w-[627px] text-[24px] dsk:text-[40px] leading-[36px] dsk:leading-[60px] font-bold">All
            your files in one secure location, accessible
            anywhere.</h1>
          <p
            class=" w-[296px] dsk:w-[585px] text-neo-desaturated-blue text-[14px] dsk:text-[17px] leading-[21px] dsk:leading-[24px] font-medium">
            Fylo stores your most important files in one secure location.
            Access them wherever you need, share and collaborate with friends,
            family, and co-workers.
          </p>
        </div>
        <div class=" flex flex-col dsk:flex-row gap-4 w-[304px] dsk:w-[536px] font-raleway">
          <div class=" flex flex-col gap-1 dsk:w-[320px]">
            <input
              class=" border border-black h-10 dsk:h-[45px] px-5 dsk:px-7 placeholder:text-neo-light-gray text-[12px] dsk:text-[14px] leading-[14px] dsk:leading-[19px] rounded-[3px]"
              :class="`${validState(isValidOne)}`" type="email" placeholder="Enter your email" v-model="emailOne">
            <h5 v-show="isValidOne == false"
              class=" text-left text-neo-red text-[10px] leading-[14px] dsk:text-xs tracking-[0.4px] font-open-sans">
              Please check your
              email</h5>
          </div>
          <button @click="checkEmailOne()"
            class=" dsk:w-[200px] h-10 dsk:h-[45px] bg-neo-bright-blue hover:bg-neo-hover-blue text-neo-grayish-blue text-[14px] leading-[16px] font-semibold rounded-[3px] shadow-lg"
            type="submit">Get Started</button>
        </div>
      </div>
    </div>
  </header>
  <main class=" mt-[130px] dsk:mt-[244px]">
    <div
      class=" relative flex flex-col dsk:flex-row-reverse dsk:justify-between items-center dsk:items-start gap-[88px] pb-20 dsk:pb-24 dsk:pt-20 bg-neo-grayish-blue">
      <img class=" absolute dsk:hidden -top-10 h-10 w-full" :src="curveMobile" alt="curveMobile">
      <img class=" absolute hidden dsk:block -top-20 h-20 w-full" :src="curveDesktop" alt="curveDesktop">
      <img class=" w-[320px] dsk:w-[542px] mt-12" :src="imgMain" alt="imgMain">
      <div class=" flex flex-col items-center dsk:items-start gap-9 dsk:gap-4 dsk:pl-20">
        <div class=" flex flex-col gap-6 dsk:gap-[38px] w-[320px] dsk:w-[650px] text-center dsk:text-left">
          <h2
            class=" text-neo-dark-blue text-[16px] dsk:text-[40px] leading-[24px] dsk:leading-[47px] font-raleway font-bold">
            Stay productive, wherever you are</h2>
          <div
            class=" flex flex-col gap-4 dsk:w-[529px] text-neo-desaturated-blue text-[14px] dsk:text-[16px] leading-[21px] dsk:leading-[24px]  font-open-sans">
            <p>
              Never let location be an issue when accessing your files. Fylo has you
              covered for all of your file storage needs.
            </p>
            <p>
              Securely share files and folders with friends, family and colleagues for
              live collaboration. No email attachments required!
            </p>
          </div>
        </div>
        <button type="button"
          class=" flex gap-2 items-center p-1 dsk:mb-[30px] text-neo-moderate-cyan text-[12px] dsk:text-[16px] leading-[16px] dsk:leading-[22px] border-b border-neo-moderate-cyan brightness-[0.9] hover:brightness-[1.25]">See
          how Fylo works
          <iconArrow />
        </button>
        <div
          class=" flex flex-col justify-center gap-3 w-[280px] dsk:w-[356px] h-[170px] dsk:h-[215px] pl-[25px] dsk:pl-[33px] pr-[12px] dsk:pr-[24px] bg-white font-open-sans rounded shadow-xl">
          <img class=" w-[14px] dsk:w-[18px]" :src="iconQuotes" alt="iconQuotes">
          <p
            class=" text-[10px] dsk:text-[13px] leading-[18px] dsk:leading-[23px] tracking-[0.38px] dsk:tracking-[0.5px] font-medium">
            Fylo has improved our team productivity by an order of magnitude. Since
            making the switch our team has become a well-oiled collaboration machine.
          </p>
          <div class=" flex items-center gap-[7px]">
            <img class=" w-6 dsk:w-8 h-6 dsk:h-8 rounded-full" :src="imgAvatar" alt="imgAvatar">
            <div class=" flex flex-col gap-[2px]">
              <h5
                class=" text-[9px] dsk:text-[11px] leading-[12px] dsk:leading-[15px] tracking-[0.45px] dsk:tracking-[0.55px] font-bold">
                Kyle Burton</h5>
              <h6
                class=" text-[6px] dsk:text-[8px] leading-[12px] dsk:leading-[15px] tracking-[0.3px] dsk:tracking-[0.4px]">
                Founder & CEO, Huddle</h6>
            </div>
          </div>
        </div>
      </div>
    </div>
    <section
      class=" flex flex-col dsk:flex-row items-center gap-6 dsk:gap-[225px] h-[345px] dsk:h-[325px] bg-neo-desaturated-blue px-12 dsk:px-20 pt-[54px] dsk:pt-[10px] text-white text-center dsk:text-left">
      <div class=" flex flex-col gap-4 w-[280px] dsk:w-[533px]">
        <h2 class=" text-[18px] dsk:text-[32px] leading-[24px] dsk:leading-[48px] font-raleway font-bold">Get early access
          today</h2>
        <p class=" text-[14px] dsk:text-[16px] leading-[21px] dsk:leading-[24px] dsk:tracking-[0.5px] font-open-sans">
          It only takes a minute to sign up and our free starter tier is extremely generous.
          If you have any questions, our support team would be happy to help you.
        </p>
      </div>
      <div class=" flex flex-col gap-2 dsk:gap-4 w-[240px] dsk:w-[480px] font-raleway">
        <div class=" flex flex-col gap-1">
          <input
            class=" w-full h-8 dsk:h-12 pl-2 dsk:pl-[22px] text-black text-[10px] dsk:text-[12px] leading-[12px] dsk:leading-[14px] border rounded-[3px]"
            :class="`${validState(isValidTwo)}`" type="email" v-model="emailTwo" placeholder="email@example.com">
          <h5 v-show="isValidTwo == false"
            class=" text-left text-[10px] leading-[14px] dsk:text-xs tracking-[0.4px] font-open-sans">Please check your
            email</h5>
        </div>
        <!-- is valid is: {{ isValidTwo }} -->
        <button @click="checkEmailTwo()"
          class=" dsk:w-[200px] h-8 dsk:h-12 bg-neo-bright-blue hover:bg-neo-hover-blue text-[10px] dsk:text-[14px] leading-[12px] dsk:leading-[16px] font-bold rounded-[3px]"
          type="submit">Get
          Started For Free</button>
      </div>
    </section>
  </main>
  <footer class=" flex flex-col gap-8 dsk:gap-9 bg-neo-dark-blue h-[590px] dsk:h-[391px] px-10 pt-16 dsk:pt-24 text-white font-open-sans">
    <img class=" w-[105px] dsk:w-[135px]" :src="logoDark" alt="logoDark">
    <div class=" flex flex-col dsk:flex-row gap-8 dsk:gap-[215px]">
      <div class=" flex flex-col gap-4 text-base">
        <div class=" flex items-center gap-4">
          <iconPhone />
          <h5>Phone: +1-543-123-4567</h5>
        </div>
        <div class=" flex items-center gap-4">
          <iconEmail />
          <h5>example@fylo.com</h5>
        </div>
      </div>
      <div class=" flex flex-col dsk:flex-row gap-8 dsk:gap-[200px] text-[16px] leading-[22px]">
        <div class=" flex flex-col gap-4">
          <TextContent content="About Us" />
          <TextContent content="Jobs" />
          <TextContent content="Press" />
          <TextContent content="Blog" />
        </div>
        <div class=" flex flex-col gap-4">
          <TextContent content="Contact Us" />
          <TextContent content="Terms" />
          <TextContent content="Privacy" />
        </div>
      </div>
      <div class=" flex justify-center gap-[10px] dsk:gap-[11px]">
        <BtnNetwork netName="facebook" />
        <BtnNetwork netName="twitter" />
        <BtnNetwork netName="instagram" />
      </div>
    </div>
  </footer>
</template>