<template>
  <section class="section">
    <div class="columns is-mobile">
      <div
        v-for="(feature, i) of features"
        :key="i"
        class="column">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title has-text-grey">
              {{ feature.title }}
            </p>
          </header>
          <div class="card-content">
            <div class="content has-text-centered">
              <!--<b-icon-->
              <!--:icon="feature.icon"-->
              <!--size="is-large"-->
              <!--type="is-primary"/>-->
              <ul style="list-style: none;text-align: justify;">
                <li>
                  <a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnb3VFUU4wQkRkbFU?usp=sharing">Semester
                    One</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnSkplQzlJdlh0RFE">Semester Two</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnUmc5Z0VBU0JEZ1E">Semester Three</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnTWh6WWEwTVZ1OFU">Semester Four</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnZENHREQ3WHYyeWM">Semester Fifth</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnWjN4aFFxcWpnSm8">Semester Sixth</a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wndG9Vc3lEOU9hZkk">Semester Seventh</a>
                </li>
              </ul>
            </div>
          </div>
          <footer class="card-footer">
            <div
              class="card-footer-item"
              v-html="feature.content"/>
          </footer>
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
        about: "Nepa~laya Publication is one of the leading book publication houses of Nepal.",
        structuredData: {
          "@context": "http://schema.org",
          "@type": "AboutPage",
          "speciality": this.about
        },
        features: [
          {
            icon: 'github-circle',
            title: 'CIST Books',
            content: `<span>more content comming soon..</span>`
          },
          // { icon: 'cellphone-link', title: 'Responsive', content: `<span><b class="has-text-grey">Every</b> component is responsive</span>` },
          // { icon: 'alert-decagram', title: 'Modern', content: `<span>Built with <a href="https://vuejs.org/">Vue.js</a> and <a href="http://bulma.io/">Bulma</a></span>` },
          // { icon: 'arrange-bring-to-front', title: 'Lightweight', content: `<span>No other internal dependency</span>` }
        ]
      }
    }, head() {
      return {
        title: 'Home',
        titleTemplate: '%s | Shikshalaya',
        __dangerouslyDisableSanitizers: ['script'],
        script: [{innerHTML: JSON.stringify(this.structuredData), type: 'application/ld+json'}]
      }
    },
  }
</script>
<style scoped>
  a {
    color: #a1a2a5;
  }
</style>
