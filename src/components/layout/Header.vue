<script setup>
import { Code2 ,Menu } from 'lucide-vue-next'
import { ref } from 'vue'
const isMenuOpen = ref(false)
const navItems = [
  { href: '#home', label: 'Home' },
  { href: '#about', label: 'About' },
  { href: '#skills', label: 'Skills' },
  { href: '#projects', label: 'Projects' },
  { href: '#contact', label: 'Contact' }
]
</script>
<template>
     <!-- Header -->
    <header class="fixed top-0 w-full bg-white/80 backdrop-blur-md border-b z-50 shadow-sm">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <a href="#home" class="flex items-center space-x-2">
            <Code2 class="h-8 w-8 text-blue-600" />
            <span class="font-bold text-xl text-gray-900">Full Stack Developer</span>
          </a>

          <!-- Desktop Navigation -->
          <nav class="hidden md:flex space-x-8">
            <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              class="text-gray-600 hover:text-blue-600 transition-colors font-medium"
            >
              {{ item.label }}
            </a>
          </nav>

          <!-- Mobile Menu Button -->
          <button 
            @click="isMenuOpen = !isMenuOpen"
            class="md:hidden p-2 rounded-md hover:bg-gray-100"
          >
            <Menu v-if="!isMenuOpen" class="h-6 w-6" />
            <X v-else class="h-6 w-6" />
          </button>
        </div>

        <!-- Mobile Navigation -->
        <nav v-if="isMenuOpen" class="md:hidden py-4 border-t">
          <div class="flex flex-col space-y-4">
            <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              class="text-gray-600 hover:text-blue-600 transition-colors font-medium"
              @click="isMenuOpen = false"
            >
              {{ item.label }}
            </a>
          </div>
        </nav>
      </div>
    </header>
</template>