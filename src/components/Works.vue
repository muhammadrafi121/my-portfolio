<!-- eslint-disable vue/multi-word-component-names -->
<template lang="">
  <div id="my-works" class="px-10 py-5">
    <h1 class="text-start text-2xl mb-3 font-bold">My Works</h1>
    <a :href="work.url" target="_blank" v-for="(work, index) in workList" :key="index">
      <div
        class="flex flex-col justify-between items-center gap-3 my-4 border-1 rounded-xl shadow-md xl:shadow-xl/30 p-3 hover:scale-102"
        :class="{
          'xl:flex-row': index % 2 === 0,
          'xl:flex-row-reverse': index % 2 !== 0,
        }"
      >
        <img class="object-cover aspect-square rounded-xl xl:w-1/3" :src="work.image" />
        <div class="xl:w-2/3">
          <h2 class="text-lg font-semibold text-start">{{ work.title }}</h2>
          <p class="text-start mb-3">{{ work.desc }}</p>
          <p class="font-semibold text-start">Tech stack:</p>
          <ul class="">
            <li v-for="(t, index) in work.tech" :key="index" class="list-disc ms-5">
              {{ t }}
            </li>
          </ul>
        </div>
      </div>
    </a>
  </div>
</template>
<script lang="ts" setup>
import { ref } from 'vue'

const workList = ref([
  {
    id: '0',
    title: 'Aplikasi Monitoring SI',
    image: '../assets/images/works/amplas.png',
    url: 'https://amplas.ptsi.co.id',
    tech: ['Bootstrap CSS', 'Vanilla Javascript', 'Laravel'],
    desc: 'Aplikasi Monitoring SI is an application used by PT. Surveyor Indonesia to monitor survey results on land that will be used in tower construction.',
  },
  {
    id: '1',
    title: 'SIMAPRES UNSRI',
    image: '../assets/images/works/simapres.png',
    url: 'https://simapres.unsri.dev',
    tech: ['Bootstrap CSS', 'Vanilla Javascript', 'Codeigniter'],
    desc: "SIMAPRES UNSRI is a platform used to record and assess the academic and extracurricular accomplishments of students. Additionally, it supports Sriwijaya University's accreditation process by adhering to relevant regulations.",
  },
  {
    id: '2',
    title: 'Telkom Avatar Teleticketing System',
    image: '../assets/images/works/telkom.png',
    url: 'https://teleticketing.dtvv.net/telkom-avatar/',
    tech: ['Bootstrap CSS', 'Vanilla Javascript', 'Codeigniter'],
    desc: "Telkom's ATS is a system used by UseeTV, Telkom Indonesia's internal division, to report service issues across Indonesia, as well as evaluate the performance and quality of its employees.",
  },
  {
    id: '3',
    title: 'PPCBK',
    image: '../assets/images/works/ppcbk.png',
    url: 'https://ppcbk.com/',
    tech: ['Bootstrap CSS', 'Vanilla Javascript', 'Codeigniter'],
    desc: 'PPCBK is a web based order monitoring system used by PT. Dok dan Perkapalan Air Kantung.',
  },
  {
    id: '4',
    title: 'Analisis Sentimen Komentar Vaksinasi Covid-19 Menggunakan Deep Learning XLNet',
    image: '../assets/images/works/sentiment-analysis.png',
    url: 'https://github.com/muhammadrafi121/analisis-sentimen-vaksinasi-covid-19',
    tech: ['Python', 'PyQT5', 'PyTorch'],
    desc: 'Developed an application to analyze public sentiment towards COVID-19 vaccination by leveraging the XLNet deep learning model.',
  },
])
</script>
<style lang=""></style>
