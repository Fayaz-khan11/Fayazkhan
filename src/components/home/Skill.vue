<script setup>
const skillCategories = [
  {
    title: 'Backend Development',
    skills: ['PHP', 'Laravel', 'MySQL', 'PostgreSQL', 'RESTful APIs','Eloquent ORM', 'Artisan CLI']
  },
  {
    title: 'Frontend Development',
    skills: ['Vue.js', 'JavaScript', 'HTML5', 'CSS3', 'Tailwind CSS', 'Bootstrap', ]
  },
  {
    title: 'Tools & Technologies',
    skills: ['Git', 'Composer', 'NPM', 'Vite', 'PHPUnit', 'Postman']
  },
]
</script>
<template>
    <section id="skills" class="py-20 bg-gray-50">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold mb-4 text-gray-900">Skills & Technologies</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            Here are the technologies and tools I work with to bring ideas to life.
          </p>
        </div>

        <div class="grid md:grid-cols- lg:grid-cols-4 gap-6 text-c">
          <div
            v-for="(category, index) in skillCategories"
            :key="index"
            class="bg-white rounded-xl p-6 shadow-sm hover:shadow-md transition-shadow"
          >
            <h3 class="text-lg font-semibold mb-4 text-gray-900">{{ category.title }}</h3>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="(skill, skillIndex) in category.skills"
                :key="skillIndex"
                class="bg-blue-100 text-blue-800 text-xs px-3 py-1 rounded-full font-medium"
              >
                {{ skill }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>