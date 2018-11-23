<template>
  <section class="section">
    <div class="columns is-mobile">
      <div
        v-for="(feature, i) of features"
        :key="i"
        class="column">
        <h5 class="card-header-title has-text-grey">
          {{ feature.title }}
        </h5>
        <div class="card-content about">
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
        about: "Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject. Our Vision is to offer pedagogically differentiated technology driven solutions that lead to critical thinking and achievement of higher learning outcomes by seamlessly integrating in-class. Our Aim is to bridge the gap between what is taught in-class using Institutional textbook driven solutions and retail at-home learning providers by seamlessly integrating both. There is no single solution provider offering an end-to-end solution in the market today.",
        structuredData: {
          "@context": "http://schema.org",
          "@type": "AboutPage",
          "speciality": "Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject. Our Vision is to offer pedagogically differentiated technology driven solutions that lead to critical thinking and achievement of higher learning outcomes by seamlessly integrating in-class. Our Aim is to bridge the gap between what is taught in-class using Institutional textbook driven solutions and retail at-home learning providers by seamlessly integrating both. There is no single solution provider offering an end-to-end solution in the market today.",
          "datePublished": "2018-09-20",
          "dateCreated": "2018-09-20",
          "dateModified": "2018-09-20",
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
<style>
  div.about {
    background: aliceblue;
  }
</style>
