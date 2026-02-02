<script setup>
import { Mail, Download, Github, Linkedin} from 'lucide-vue-next'
import myPhoto from '../../assets/images/my_photo.jpg';
import my_cv from '../../assets/my-cv/Fayaz khan.pdf';

const contact_nav = [
  {href: '#contact'},
];


</script>
<template>
     <section id="home" class="pt-16 min-h-screen flex items-center bg-gradient-to-br from-blue-50 to-indigo-100">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid lg:grid-cols-2 gap-12 items-center">
          <div class="space-y-8">
            <div class="space-y-4">
              <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold leading-tight text-gray-900">
                Hi, I'm <span class="text-blue-600">Fayaz khan</span>
              </h1>
              <h2 class="text-xl sm:text-2xl text-gray-600 font-semibold">Full Stack Developer</h2>
              <p class="text-lg text-gray-600 max-w-2xl leading-relaxed">
                Passionate PHP Laravel & Vue.js developer with expertise in building scalable web applications. 
                I create modern, responsive solutions that deliver exceptional user experiences.
              </p>
            </div>

            <div class="flex flex-wrap gap-4">
              <a href="#contact" class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-lg font-semibold transition-colors flex items-center gap-2">
                <Mail class="h-4 w-4" />
                Get In Touch
              </a>
              <a 
                :href="my_cv" 
                download="Fayaz Khan.pdf"
                class="border-2 border-blue-600 text-blue-600 hover:bg-blue-600 hover:text-white px-8 py-3 rounded-lg font-semibold transition-colors flex items-center gap-2"
              >
                <Download class="h-4 w-4" />
                Download CV
            </a>
            </div>
            <div class="flex space-x-4">
              <a href="https://github.com/Fayaz-khan11" class="p-3 rounded-full bg-white shadow-md hover:shadow-lg transition-shadow">
                <Github class="h-5 w-5 text-gray-700" />
              </a>
              <a href="https://www.linkedin.com/in/fayaz-khan-320604213/" class="p-3 rounded-full bg-white shadow-md hover:shadow-lg transition-shadow">
                <Linkedin class="h-5 w-5 text-gray-700" />
              </a>
            </div>
          </div>

          <div class="relative">
            <div class="relative w-80 h-80 mx-auto">
              <div class="absolute inset-0 bg-gradient-to-r from-blue-400 to-purple-500 rounded-full blur-3xl opacity-20"></div>
              <img
                :src="myPhoto"
                alt="Developer Portrait"
                class="relative z-10 w-full h-full rounded-full object-cover border-4 border-white shadow-2xl"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
</template>