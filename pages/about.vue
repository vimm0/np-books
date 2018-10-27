<template>
  <section class="section">
    <div class="columns is-mobile">
      <div
        v-for="(feature, i) of features"
        :key="i"
        class="column">
            <p class="card-header-title has-text-grey">
              {{ feature.title }}
            </p>
          <div class="card-content" style="background:aliceblue;">
            <div class="content has-text-centered">
              <p>{{about}}</p>
            </div>
          </div>
      </div>
    </div>
  </section>
</template>

<script>
  import BLogo from '@/components/Logo'

  export default {
    name: 'HomePage',
    components: {BLogo},
    data() {
      return {
        about: "Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject.",
        structuredData: {
          "@context": "http://schema.org",
          "@type": "AboutPage",
          "speciality": this.about
        },
        features: [
          {
            title: 'About',
            content: `<span>more content comming soon..</span>`
          },
          // { icon: 'cellphone-link', title: 'Responsive', content: `<span><b class="has-text-grey">Every</b> component is responsive</span>` },
        ]
      }
    }, head() {
      return {
        title: 'About',
        titleTemplate: '%s | Shikshalaya',
        __dangerouslyDisableSanitizers: ['script'],
        script: [{innerHTML: JSON.stringify(this.structuredData), type: 'application/ld+json'}]
      }
    },
  }
</script>
