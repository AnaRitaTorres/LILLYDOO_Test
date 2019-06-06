<template>
  <div id="app">
    <Header/>
    <Trialbox @testPaket="wipesType"/>
    <Faqs/>
    <TrialboxContent :wipes="wipes"/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Trialbox from '@/components/Trialbox.vue'
import Faqs from '@/components/Faqs.vue'
import TrialboxContent from '@/components/TrialboxContent.vue'

export default {
  name: 'App',
  components: {
    Header,
    Trialbox,
    Faqs,
    TrialboxContent
  },
  data() {
    return {
      wipes: null
    }
  },
  mounted() {
    this.wipesType();
  },
  methods: {
    wipesType(wipes) {
      console.log(wipes)
      this.wipes = wipes;
    }
  }
}
</script>

<style lang="scss">

$divMargin: 0;
$divPadding: 0;

$fontFamily: CeraPro,Helvetica,Roboto,Arial,sans-serif !important;
$fontWeight: 400 !important;
$color: #000 !important;

$rowMargin: 0 auto !important;
$rowPadding: 2rem 0 2rem 0;
$rowWidth: 100%;

$bright: #fff;
$dark: #f8f8f8;
$classPadding: 1.25rem 0;

$textAlign: center !important;

$logoTop: 8%;
$logoRight: 3%;
$logoWidth: 12%;
$logoPosition: absolute;

$marginBottom10: 10px !important;
$marginBottom20: 20px !important;
$marginBottom30: 30px !important;

$uppercase: uppercase;


div {
  margin: $divMargin;
  padding: $divPadding;
}

body {
  font-family: $fontFamily;
  font-weight: $fontWeight;
  color: $color;
}

img {
  width: 100%;
}

.rows {
  margin: $rowMargin;
  padding: $rowPadding;
  width: $rowWidth;
}

.bright {
  background-color: $bright;
  padding: $classPadding;
}

.dark {
  background-color: $dark;
  padding: $classPadding;
}

.text-center {
  text-align: $textAlign;
}

.oekotex_logo {
  top: $logoTop;
  right: $logoRight;
  width: $logoWidth;
  position: $logoPosition;
}

.margin-bottom-10 {
  margin-bottom: $marginBottom10;
}

.margin-bottom-20 {
  margin-bottom: $marginBottom20;
}

.margin-bottom-30 {
  margin-bottom: $marginBottom30;
}

.uppercase {
  text-transform: $uppercase;
}


</style>
