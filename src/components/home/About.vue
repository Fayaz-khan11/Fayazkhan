<script setup>
import { Code2, Database, Globe, Zap } from 'lucide-vue-next'
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

</script>
<template>
     <section id="about" class="py-20 bg-white">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold mb-4 text-gray-900">About Me</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            I'm a dedicated full-stack developer with a passion for creating innovative web solutions using modern technologies.
          </p>
        </div>

        <div class="grid lg:grid-cols-2 gap-12 items-center">
          <div class="space-y-6">
            <p class="text-gray-600 leading-relaxed">
              With extensive experience in PHP Laravel and Vue.js, I specialize in building robust web applications that 
              solve real-world problems. My journey in web development has equipped me with a deep understanding of both 
              backend and frontend technologies.
            </p>
            <p class="text-gray-600 leading-relaxed">
              I'm passionate about writing clean, efficient code and staying up-to-date with the latest industry trends. 
              Whether it's developing RESTful APIs, creating interactive user interfaces, or optimizing database performance, 
              I approach each project with attention to detail and a commitment to excellence.
            </p>
            <div class="flex flex-wrap gap-8 pt-4">
              <div class="text-center">
                <div class="text-3xl font-bold text-blue-600">5+</div>
                <div class="text-sm text-gray-600 font-medium">Projects Completed</div>
              </div>
              <div class="text-center">
                <div class="text-3xl font-bold text-blue-600">3+</div>
                <div class="text-sm text-gray-600 font-medium">Years Experience</div>
              </div>
              <div class="text-center">
                <div class="text-3xl font-bold text-blue-600">100%</div>
                <div class="text-sm text-gray-600 font-medium">Manager Satisfaction</div>
              </div>
            </div>
          </div>

          <div class="grid sm:grid-cols-2 gap-6">
            <div
              v-for="(highlight, index) in highlights"
              :key="index"
              class="bg-gray-50 rounded-xl p-6 text-center hover:shadow-lg transition-shadow"
            >
              <component :is="highlight.icon" class="h-12 w-12 text-blue-600 mx-auto mb-4" />
              <h3 class="font-semibold mb-2 text-gray-900">{{ highlight.title }}</h3>
              <p class="text-sm text-gray-600">{{ highlight.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>