<script setup>
import Header from './Header.vue'
import Footer from './Footer.vue'
import Hero from '../home/Hero.vue'
import About from '../home/About.vue'
import Skill from '../home/Skill.vue'
import Projects from '../home/Projects.vue'
import Contact from '../home/Contact.vue'
import { ref } from 'vue'
import { 
  Code2, Menu, X, Mail, Download, Github, Linkedin, Twitter,
  ExternalLink, Send, Phone, MapPin, Database, Globe, Zap,
  Quote, Star, ChevronLeft, ChevronRight
} from 'lucide-vue-next'

const isMenuOpen = ref(false)

const highlights = [
  {
    icon: Code2,
    title: 'Clean Code',
    description: 'Writing maintainable and scalable code following best practices'
  },
  {
    icon: Database,
    title: 'Database Design',
    description: 'Efficient database architecture and optimization'
  },
  {
    icon: Globe,
    title: 'Full Stack',
    description: 'End-to-end development from backend APIs to frontend interfaces'
  },
  {
    icon: Zap,
    title: 'Performance',
    description: 'Optimized applications with fast loading times'
  }
]

// Start autoplay when component mounts
import { onMounted, onUnmounted } from 'vue'

</script>
<template>
        <Header />
        <Hero />
        <About />
        <Skill />
        <Projects />
        <Contact />
        <Footer />
</template>

<style scoped>
html {
  scroll-behavior: smooth;
}

.container {
  max-width: 1200px;
}

</style>