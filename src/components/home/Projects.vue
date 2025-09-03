<script setup>
import ntcImage from '../../assets/images/ntc_login_1.png';
import ntxImage2 from '../../assets/images/ntc_login_2.png';
import kicTech from '../../assets/images/kim_tech.png';
import respiratoryZone from '../../assets/images/respiratory.png';
import countyMedical from '../../assets/images/county_medical.png';
const projects = [
    {
        title: 'University Accreditation Management System',
        description: 'Built a comprehensive system for managing university accreditation processes, aligned with HEC (Higher Education Commission) standards. The platform included modules for student management, AIC evaluations, document tracking, and institutional self-assessment.',
        image: `${ntcImage}`,
        technologies: ['Laravel', 'React', 'MySQL', 'RESTful APIs','Eloquent ORM', 'Artisan CLI'],
        link: 'https://accreditation-ntc.hec.gov.pk/login'
    },
    {
        title: 'Student Accreditation Management System',
        description: 'Accreditation ensures that quality technology education programs comparable to international standards are run in all universities of the country. The Accreditation process gives the Institute an opportunity to conduct in-depth analysis of its strengths and weaknesses in its internal and external environments and protects and promotes the interest of all stakeholders',
        image: `${ntxImage2}`,
        technologies: ['Laravel','Javascript','Css/Bootstrap','MySQL','Eloquent ORM', 'Artisan CLI'],
        link: 'https://registration-ntc.hec.gov.pk/login'
    },
    {
        title: 'Kim Tech',
        description: 'The system allows users to create, manage, and track invoices and quotations efficiently. Key features include customer management, real-time calculation of taxes and totals, PDF generation, and status tracking (paid/unpaid). Contributed to both frontend UI development and backend logic for data handling and validation.',
        image: `${kicTech}`,
        technologies: ['Laravel', 'Eloquent ORM', 'Artisan CLI','Vue.js', 'Mysql', 'css /Bootstrap'],
        link:'https://portal.hitec-tw.com/login'
    },
    {
        title: 'Respiratoy Zone',
        description: 'The platform includes modules for creating and managing quotations, handling inventory, and tracking orders. Built a custom admin dashboard using Chart.js for real-time analytics and reporting. Contributed to both frontend and backend development, focusing on user experience, data accuracy, and business logic.',
        image: `${respiratoryZone}`,
        technologies: ['Laravel', 'Javascript', 'MySQL', 'Css/Bootstrap' ,'Chart.js'],
        link: 'https://portal.respiratoryzone.pk/login'
    },
    {
        title: 'County Medical Management System',
        description: 'Developed a healthcare platform to manage patient-doctor interactions at the county level. The system featured doctor and patient registration, appointment scheduling, medical history tracking, and prescription management. Designed for scalability and ease of use by medical staff, with secure access controls and real-time notifications.',
        image: `${countyMedical}`,
        technologies: ['Laravel', 'Javascript', 'MySQL', 'Css/Bootstrap' ,'Chart.js'],
        link: 'https://countymedical.co.uk/'
    },
]
</script>
<template>
     <section id="projects" class="py-20 bg-white">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold mb-4 text-gray-900">Featured Projects</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            Here are some of the projects I've worked on that showcase my skills in Laravel and Vue.js development.
          </p>
        </div>

        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="(project, index) in projects"
            :key="index"
            class="bg-white rounded-xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-300 group"
          >
            <div class="relative overflow-hidden">
              <img
                :src="project.image"
                :alt="project.title"
                class="w-full h-48 object-cover group-hover:scale-105 transition-transform duration-300"
              />
              <div
                class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center space-x-4"
              >
                <a
                  :href="project.link"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="bg-white text-gray-900 px-4 py-2 rounded-lg font-medium flex items-center gap-2 hover:bg-gray-100 transition-colors"
                >
                  <ExternalLink class="h-4 w-4" />
                  Live Demo
                </a>
              </div>

            </div>
            <div class="p-6">
              <h3 class="text-xl font-semibold mb-2 text-gray-900">{{ project.title }}</h3>
              <p class="text-gray-600 mb-4">{{ project.description }}</p>
              <div class="flex flex-wrap gap-2">
                <span
                  v-for="(tech, techIndex) in project.technologies"
                  :key="techIndex"
                  class="border border-gray-200 text-gray-700 text-xs px-2 py-1 rounded font-medium"
                >
                  {{ tech }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>