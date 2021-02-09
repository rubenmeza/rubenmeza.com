<template>
  <!-- <section class="hero is-light is-fullheight">
    <div class="hero-body">
      <div class="container">
        <div class="columns">
          <div class="column">
            <h1 class="title">Hey there!</h1>
            <h1 class="title">I'm Ruben Meza</h1>
            <h2 class="subtitle">FULL STACK DEVELOPER</h2>
            <h3 class="subtitle">Site made with love and vue</h3>
            <a href="https://www.linkedin.com/in/rubenmezarazo/" target="blank">
              <i class="fab fa-linkedin-in"></i>
            </a>
            &nbsp;&nbsp;
            <a href="https://gitlab.com/ruben.meza" target="blank">
              <i class="fab fa-gitlab"></i>
            </a>
            &nbsp;&nbsp;
            <a href="https://github.com/rubenmeza" target="blank">
              <i class="fab fa-github"></i>
            </a>
            &nbsp;&nbsp;
            <a href="https://twitter.com/_SoyUnPollo" target="blank">
              <i class="fab fa-twitter"></i>
            </a>
            &nbsp;&nbsp;
            <a href="mailto:rmezar@gmail.com" target="blank">
              <i class="fas fa-at"></i>
            </a>
          </div>
          <div class="column">
            <h2 class="subtitle">Skills</h2>
            <div class="tags">
              <span class="tag is-white">nodejs</span>
              <span class="tag is-white">golang</span>
              <span class="tag is-white">vuejs</span>
              <span class="tag is-white">git</span>
              <span class="tag is-white">docker</span>
              <span class="tag is-white">grpc</span>
              <span class="tag is-white">micro services</span>
              <span class="tag is-white">bitcoin</span>
              <span class="tag is-white">blockchain</span>
              <span class="tag is-white">firebase</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section> -->
<div class="min-h-screen p-6 flex flex-col flex-wrap place-content-center">
  <div class="flex flex-grow flex-wrap flex-items-center content-end place-content-center py-5">
    <h1 class="block font-semibold text-4xl">Hello, I'm Ruben Meza</h1>
  </div>
  <div class="w-2/3 -m-2 flex-grow">
    <p>
      I build things using software by day, and train to be a hacker by night, I love to fix things make things, and solve problems, I also love playing video games like Call of Duty. Do you want to know more about me? <a class="tracking-wide text-sm text-indigo-500 font-semibold" href="https://calendly.com/rubenmeza/hablando-de-software" target="blank">lets talk</a>
    </p>
  </div>
  <!-- <div class="flex flex-grow flex-wrap content-end">
    <h3 class="">Skills</h3>
  </div> -->
  <div class="w-2/3 flex flex-grow flex-wrap content-center place-content-center p-4">
    <!-- <div class="col-span-5 font-semibold">soft skills</div> -->
    <tag v-for="skill in skillList" class="flex-initial m-2" :key="skill">{{ skill }}</tag>
  </div>
  <div class="w-2/3 flex flex-grow flex-wrap content-center place-content-center">
    <button class="py-2 px-4 bg-gray-500 text-white font-semibold rounded-lg shadow-md hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-400 focus:ring-opacity-75">
      resume
    </button>
  </div>
  <div class="w-2/3 flex flex-row">
    <a class="flex-1" href="https://www.linkedin.com/in/rubenmezarazo/" target="blank">
      <i class="fab fa-linkedin-in"></i>
    </a>
    <a class="flex-1 flex-grow" href="https://gitlab.com/ruben.meza" target="blank">
      <i class="fab fa-gitlab"></i>
    </a>
    <a class="flex-1 flex-grow" href="https://github.com/rubenmeza" target="blank">
      <i class="fab fa-github"></i>
    </a>
    <a class="flex-1 flex-grow" href="https://twitter.com/_SoyUnPollo" target="blank">
      <i class="fab fa-twitter"></i>
    </a>
    <a class="flex-1 flex-grow" href="mailto:rmezar@gmail.com" target="blank">
      <i class="fas fa-at"></i>
    </a>
  </div>
</div>
</template>

<script>
import shuffle from 'lodash/shuffle'
import Tag from '@/components/Tag.vue'

export default {
  name: 'Home',
  components: {
    Tag
  },
  data () {
    return {
      skills: [
        'Problem Solving',
        'Security',
        'Automation',
        'Collaboration',
        'Best Practices',
        'Node.js',
        'Golang',
        'Vue.js',
        'Microservices',
        'Bitcoin',
        'Git',
        'Docker',
        'GRPC',
        'firebase',
        'mongodb',
        'MySql'
      ]
    }
  },
  computed: {
    skillList () {
      return shuffle(this.skills)
    }
  }
}
</script>
