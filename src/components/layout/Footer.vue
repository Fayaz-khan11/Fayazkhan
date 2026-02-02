
<script setup>
import { Twitter ,Linkedin, Github, Code2 } from 'lucide-vue-next'
</script>

<template>
     <footer class="bg-gray-900 text-white">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        <div class="grid md:grid-cols-3 gap-8">
          <div class="space-y-4">
            <div class="flex items-center space-x-2">
              <Code2 class="h-8 w-8 text-blue-400" />
              <span class="font-bold text-xl">Full Stack Developer</span>
            </div>
            <p class="text-gray-400 leading-relaxed">
              Full Stack Developer specializing in Laravel and Vue.js. Creating modern web solutions that make a difference.
            </p>
          </div>

          <div class="space-y-4">
            <h3 class="font-semibold text-lg">Quick Links</h3>
            <div class="space-y-2">
              <a href="#home" class="block text-gray-400 hover:text-white transition-colors">Home</a>
              <a href="#about" class="block text-gray-400 hover:text-white transition-colors">About</a>
              <a href="#skills" class="block text-gray-400 hover:text-white transition-colors">Skills</a>
              <a href="#projects" class="block text-gray-400 hover:text-white transition-colors">Projects</a>
              <a href="#contact" class="block text-gray-400 hover:text-white transition-colors">Contact</a>
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="font-semibold text-lg">Connect</h3>
            <div class="flex space-x-3">
              <a href="https://github.com/Fayaz-khan11" target="_blank" class="p-2 bg-gray-800 rounded-lg hover:bg-gray-700 transition-colors">
                <Github class="h-5 w-5" />
              </a>
              <a href="www.linkedin.com/in/fayaz-khan-320604213" target="_blank" class="p-2 bg-gray-800 rounded-lg hover:bg-gray-700 transition-colors">
                <Linkedin class="h-5 w-5" />
              </a>
              <a href="" class="p-2 bg-gray-800 rounded-lg hover:bg-gray-700 transition-colors">
                <Twitter class="h-5 w-5" />
              </a>
            </div>
          </div>
        </div>

        <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
          <p>&copy; {{ new Date().getFullYear() }} Fayaz khan. All rights reserved.</p>
        </div>
      </div>
    </footer>
</template>