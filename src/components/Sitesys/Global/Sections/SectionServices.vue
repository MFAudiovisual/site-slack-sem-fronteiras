<template>
  <section id="services" class="services">
    <div class="container py-24 mx-auto px-4">
      <div class="anim3-scroll">
        <h2 class="trigger3-scroll text-7xl md:text-5xl mb-10 text-center">
          Serviços
        </h2>
        <div
          class="lg:w-full mx-auto flex flex-wrap justify-center items-center"
        >
          <div class="w-full lg:py-6 mt-6 lg:mt-0">
            <div class="grid lg:grid-cols-2 gap-6">
              <div
                v-for="item in servicesList"
                :key="item.id"
                class="p-3 bg-light dark:bg-extra-dark/40 dark:text-gray-300 shadow rounded-lg px-5 py-6"
              >
                <img :src="item.src" class="w-full mb-4" />
                <a :href="item.href">
                  <span class="font-bold text-xl">{{ item.title }}</span>
                </a>

                <p class="my-2 text-justify text-sm">
                  {{ item.description }}
                </p>

                <a
                  :href="item.href"
                  class="flex flex-row items-center mt-3 text-blue-600 hover:text-blue-800"
                >
                  <span>Veja mais detalhes...</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import imgUrl1 from '@/assets/images/sitesys/gallery/image-05.jpg'
import imgUrl2 from '@/assets/images/sitesys/gallery/image-02.jpg'
import imgUrl3 from '@/assets/images/sitesys/gallery/image-06.jpg'
import imgUrl4 from '@/assets/images/sitesys/gallery/image-04.jpg'
import imgUrl5 from '@/assets/images/sitesys/gallery/image-05.jpg'
import imgUrl6 from '@/assets/images/sitesys/gallery/image-06.jpg'

const servicesList = [
  {
    id: '1',
    title: 'Oficinas de Slackline',
    description:
      'Com experiência e dedicação fazemos jus ao nosso lema “O SLACK QUE UNE PESSOAS”. Criamos uma atmosfera lúdica, saudável e agradável em que os participantes se sentem motivados a entrar na brincadeira e experimentar essa aventura. O público cria uma empatia forte com o evento através da INTERAÇÃO e COMPARTILHAMENTO de EMOÇÃO.',
    src: imgUrl1,
    href: '#',
  },
  {
    id: '2',
    title: 'Trickline',
    description:
      'Sem dúvida, é um entretenimento espetacular, porque tricklining é a disciplina mais dinâmica do slackline e combina o ar livre com o freestyle urbano. Força, coordenação, resistência e estilo são cruciais nos saltos acrobáticos de até sete metros de altura, combos aparentemente intermináveis e truques estáticos exigentes. A comunidade e a vibração são importantes para muitos atletas incentivando nos truques e combos espetaculares.',
    src: imgUrl2,
    href: '#',
  },
  {
    id: '3',
    title: 'Highline',
    description:
      'Coloque uma pitada de energia radical extra com as apresentações de HIGHLINE! Aqui, os atletas desafiam a gravidade colocando a fita de Slackline nas alturas. Atividade requer alta qualidade técnica e equipamentos próprios para ser realizada com segurança e beleza. É a Arte do Equilíbrio na sua modalidade mais pura.',
    src: imgUrl3,
    href: '',
  },
  {
    id: '4',
    title: 'Slack Park',
    description:
      'O Slackline a cada dia vem trazendo novos adeptos e curiosos de como se equilibrar na fita, porém a falta de acesso a informação e um lugar especifico para a pratica, acaba sendo uma dificuldade para incluir o slackline como uma nova proposta de entretenimento para sua empresa. O Slack Park é um espaço exclusivo para o slackline, promovendo saúde e bem-estar, onde o slack se transforma em um local de reunião, alegria e aprendizagem para todos.',
    src: imgUrl4,
    href: '#',
  },
]
</script>
