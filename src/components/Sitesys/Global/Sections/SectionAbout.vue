<template>
  <img
    alt="Image"
    class="mx-auto my-12 w-[20vh] h-[20vh] max-w-auto object-cover object-center rounded"
    :src="imageUrl2"
  />
  <section id="about" class="about">
    <div class="container py-24 mx-auto px-4">
      <div class="anim1-scroll">
        <h2 class="trigger1-scroll text-7xl md:text-5xl mb-10 text-center">
          Sobre
        </h2>
        <div
          class="lg:w-full mx-auto flex flex-wrap justify-center items-center"
        >
          <img
            alt="Image"
            class="w-[480px] h-[480px] max-w-auto lg:pl-10 lg:py-6 mt-6 lg:mt-0 object-cover object-center rounded"
            :src="imageUrl1"
          />
          <div class="lg:w-1/2 w-full lg:pl-10 lg:py-6 mt-6 lg:mt-0">
            <p class="text-base text-center lg:text-left">
              Apaixonados por
              <span class="text-brand-800 font-semibold">SLACKLINE </span>
              , vemos nele mais que um esporte, mas um estilo de vida diferente
              que te permite despertar para o equilíbrio que existe em cada um
              de nós, vivenciando diversas experiências, superando seus limites
              e incentivando mais pessoas a buscar novos horizontes e conexões.
            </p>
            <br />
            <p class="text-base text-center lg:text-left">
              <span class="text-brand-800 font-semibold">
                SLACK SEM FRONTEIRAS
              </span>
              Criada por um casal de educadores e slackliners a mais de dez
              anos, somos pioneiros em compartilhar a prática do slackline,
              desenvolvendo técnicas inovadoras, criativas e divertidas de se
              equilibrar na fita, proporcionando experiências inesquecíveis,
              fomentando e compartilhando o esporte e a arte do equilíbrio,
              unindo cada vez mais pessoas em busca de uma vida equilibrada e
              saudável.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import imageUrl1 from '@/assets/images/sitesys/about/about-01.jpg'
import imageUrl2 from '@/assets/images/sitesys/logo/logo.png'
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  gsap.from('.anim1-scroll', {
    y: 100,
    opacity: 0,
    duration: 0.5,
    ease: 'power3.inOut',
    scrollTrigger: {
      trigger: '.trigger1-scroll',
      start: 'top 80%',
      end: 'center 10%',
      toggleActions: 'play none resume complete',
      markers: false,
    },
  })
})
</script>
