<template>
  <main>
    <SitesysNavbar />
    <SectionHome />
    <SectionAbout />
    <ParallaxMulti :sliders="sliderImg" size="84vh" />
    <SectionPhotos />
    <SliderImage
      size="72vh"
      :sliders="sliderImg1"
      background-color="#0000001a"
    />
    <SectionVideos />
    <ParallaxStatic :image="imageUrl2" />
    <SectionServices />
    <SectionContact />
    <ScrollToTop />
    <SitesysFooter />
  </main>
</template>

<script setup>
import SitesysNavbar from '@/components/Sitesys/Global/SitesysNavbar/SitesysNavbar.vue'
import SitesysFooter from '@/components/Sitesys/Global/SitesysFooter/SitesysFooter.vue'
import ScrollToTop from '@/components/Sitesys/Global/ScrollToTop/ScrollToTop.vue'
import SectionHome from '@/components/Sitesys/Global/Sections/SectionHome.vue'
import SectionAbout from '@/components/Sitesys/Global/Sections/SectionAbout.vue'
import SectionPhotos from '@/components/Sitesys/Global/Sections/SectionPhotos.vue'
import SectionVideos from '@/components/Sitesys/Global/Sections/SectionVideos.vue'
import SectionServices from '@/components/Sitesys/Global/Sections/SectionServices.vue'
import SectionContact from '@/components/Sitesys/Global/Sections/SectionContact.vue'
import ParallaxStatic from '@/components/Sitesys/Global/Parallax/ParallaxStatic.vue'
import ParallaxMulti from '@/components/Sitesys/Global/Parallax/ParallaxMulti.vue'
import SliderImage from '@/components/Sitesys/Global/Slider/SliderImage.vue'

import imgUrl1 from '@/assets/images/sitesys/sliders/image-01.jpg'
import imgUrl2 from '@/assets/images/sitesys/sliders/image-02.jpg'
import imgUrl3 from '@/assets/images/sitesys/sliders/image-03.jpg'
import imgUrl4 from '@/assets/images/sitesys/sliders/image-04.jpg'

import imageUrl1 from '@/assets/images/sitesys/parallax/parallax-01.jpg'
import imageUrl2 from '@/assets/images/sitesys/parallax/parallax-02.jpg'

const sliderImg = [
  {
    id: '1',
    title: 'O que se aprende ao praticar SLACKLINE?',
    description: '',
    actionLabel: '',
    actionUrl: '/',
    image: imgUrl1,
  },
  {
    id: '2',
    title: '',
    description: 'DIVERSÃO, EQUILÍBRIO, CONEXÃO...',
    actionLabel: '',
    actionUrl: '/',
    image: imgUrl2,
  },
]

const sliderImg1 = [
  {
    id: '1',
    title: '',
    description: '',
    actionLabel: '',
    actionUrl: '/',
    image: imgUrl3,
  },
  {
    id: '2',
    title: '',
    description: '',
    actionLabel: '',
    actionUrl: '/',
    image: imgUrl4,
  },
]
</script>
