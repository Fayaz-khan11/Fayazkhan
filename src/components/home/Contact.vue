<script setup>
import { ref } from 'vue'
import { Send, Phone, MapPin ,Mail ,ExternalLink ,Github ,Linkedin ,Twitter } from 'lucide-vue-next'
import emailjs from 'emailjs-com'

const form = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const submitForm = () => {
  const templateParams = {
    name: form.value.name,
    email: form.value.email,
    subject: form.value.subject,
    message: form.value.message,
  };

  emailjs.send(
    'service_a5lkmq9',
    'template_yay09no',
    templateParams,
    'KPC9F39M-hH8ujwET'
  ).then(() => {
    alert('✅ Email sent successfully!')
    form.value = { name: '', email: '', subject: '', message: '' }
  }).catch((err) => {
    console.error(err)
    alert('❌ Failed to send email')
  })
}

const contactInfo = [
  {
    icon: Mail,
    title: 'Email',
    value: 'fayaz.fk8184@gmail.com',
    href: 'mailto:your.email@example.com'
  },
  {
    icon: Phone,
    title: 'Phone',
    value: '03481997319',
    href: 'tel:+15551234567'
  },
  {
    icon: MapPin,
    title: 'Location',
    value: 'Islamabad, Pakistan',
    href: '#'
  }
]
</script>
<template>
    <section id="contact" class="py-20 bg-gray-50">
      <div class="container mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold mb-4 text-gray-900">Get In Touch</h2>
          <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            Ready to start your next project? Let's discuss how I can help bring your ideas to life with Laravel and Vue.js.
          </p>
        </div>

        <div class="grid lg:grid-cols-2 gap-12">
          <div class="space-y-8">
            <div>
              <h3 class="text-2xl font-semibold mb-4 text-gray-900">Let's Work Together</h3>
              <p class="text-gray-600 mb-6 leading-relaxed">
                I'm always interested in new opportunities and exciting projects. Whether you need a full-stack web 
                application, API development, or consultation on your existing Laravel/Vue.js project, I'd love to hear from you.
              </p>
            </div>

            <div class="space-y-4">
              <div
                v-for="(info, index) in contactInfo"
                :key="index"
                class="flex items-center space-x-4"
              >
                <div class="flex-shrink-0">
                  <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center">
                    <component :is="info.icon" class="h-6 w-6 text-blue-600" />
                  </div>
                </div>
                <div>
                  <h4 class="font-medium text-gray-900">{{ info.title }}</h4>
                  <a :href="info.href" class="text-gray-600 hover:text-blue-600 transition-colors">
                    {{ info.value }}
                  </a>
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white rounded-xl p-8 shadow-sm">
            <h3 class="text-xl font-semibold mb-2 text-gray-900">Send Message</h3>
            <p class="text-gray-600 mb-6">Fill out the form below and I'll get back to you as soon as possible.</p>
            
            <form @submit.prevent="submitForm" class="space-y-4">
              <div class="grid sm:grid-cols-2 gap-4">
                <input
                  v-model="form.name"
                  type="text"
                  placeholder="Your Name"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none transition-colors"
                />
                <input
                  v-model="form.email"
                  type="email"
                  placeholder="Your Email"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none transition-colors"
                />
              </div>
              <input
                v-model="form.subject"
                type="text"
                placeholder="Subject"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none transition-colors"
              />
              <textarea
                v-model="form.message"
                placeholder="Your Message"
                rows="5"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none transition-colors resize-none"
              ></textarea>
              <button
                type="submit"
                class="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 rounded-lg font-semibold transition-colors flex items-center justify-center gap-2"
              >
                <Send class="h-4 w-4" />
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>
</template>