<template>
  <div>
    <myheader />
    <nuxt />
    <myfooter />
  </div>
</template>

<script>
import myheader from '../components/Header.vue'
import myfooter from '../components/Footer.vue'


export default {
  name: 'defaultpage',
  components: { myheader , myfooter }
}
</script>

<style>
@font-face {
    font-family: IRANSans;
    font-style: normal;
    font-weight: normal;
    src: url('~assets/fonts/IRANSansFaNum.woff') format('woff');
    /* FF3.6+, IE9, Chrome6+, Saf5.1+*/
}

@font-face {
    font-family: IRANSans;
    font-style: normal;
    font-weight: 100;
    src: url('~assets/fonts/IRANSansFaNum_Light.woff') format('woff');
    /* FF3.6+, IE9, Chrome6+, Saf5.1+*/
}

@font-face {
    font-family: IRANSans;
    font-style: normal;
    font-weight: bold;
    src: url('~assets/fonts/IRANSansFaNum_Bold.woff') format('woff');
    /* FF3.6+, IE9, Chrome6+, Saf5.1+*/
}

@font-face {
    font-family: IRANSans;
    font-style: normal;
    font-weight: 400;
    src: url('~assets/fonts/IRANSansFaNum_Medium.woff') format('woff');
    /* FF3.6+, IE9, Chrome6+, Saf5.1+*/
}

@font-face {
    font-family: IRANSans;
    font-style: normal;
    font-weight: 900;
    src: url('~assets/fonts/IRANSansFaNum_Black.woff') format('woff');
    /* FF3.6+, IE9, Chrome6+, Saf5.1+*/
}

body{
  font-family: IRANSans, sans-serif;
  direction: rtl;
  text-align: right;
  font-size: 14px;
  line-height: 24px;
}
  
</style>
