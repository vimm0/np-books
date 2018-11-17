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
              <ul class="sem-list">
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
              <p>Share</p>
              <a :href="`https://www.facebook.com/sharer/sharer.php?u=${url}&amp;src=sdkpreparse`"
                 target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24">
                  <path
                    d="M12 0a12 12 0 1 0 0 24 12 12 0 0 0 0-24zm3 8h-1.35c-.54 0-.65.22-.65.78V10h2l-.2 2H13v7h-3v-7H8v-2h2V7.7c0-1.78.93-2.7 3.03-2.7H15v3z"/>
                </svg>
              </a>
              <a :href="`https://twitter.com/intent/tweet?url=${url};`">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24">
                  <path
                    d="M12 0a12 12 0 1 0 0 24 12 12 0 0 0 0-24zm6.07 9.64A8.12 8.12 0 0 1 9.9 18.2a8.13 8.13 0 0 1-4.4-1.3 5.78 5.78 0 0 0 4.25-1.18 2.88 2.88 0 0 1-2.68-2c.45.09.9.06 1.3-.05a2.88 2.88 0 0 1-2.3-2.85c.38.22.82.35 1.3.36a2.88 2.88 0 0 1-.9-3.83 8.15 8.15 0 0 0 5.92 3 2.88 2.88 0 0 1 4.9-2.62 5.73 5.73 0 0 0 1.82-.7 2.88 2.88 0 0 1-1.26 1.59 5.73 5.73 0 0 0 1.65-.45 5.77 5.77 0 0 1-1.43 1.49z"/>
                </svg>
              </a>
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
        structuredData: {
          "@context": "http://schema.org",
          "@type": "WebSite",
          "about": "Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject.",
          "keywords": "shikshalaya Shikshalaya cist CSIT Csit Csit 1st 2nd 3rd 4th 5th 6th 7th 8th first second third fourth fifth sixth seventh eight semester Semester",
          "genre": "Education",
          "datePublished": "2018-09-20",
          "dateCreated": "2018-09-20",
          "dateModified": "2018-09-20",
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
        ],
        url: process.env.HOST_URL + this.$route.path
      }
    },
    head() {
      return {
        title: 'Home',
        titleTemplate: '%s | Shikshalaya',
        __dangerouslyDisableSanitizers: ['script'],
        script: [{innerHTML: JSON.stringify(this.structuredData), type: 'application/ld+json'}],
        meta: [{
          'og:url': this.url || '',
        }]
      }
    },
  }
</script>
<style scoped>
  a {
    color: #a1a2a5;
  }

  ul.sem-list {
    list-style: none;
    text-align: justify;
  }
</style>
