<template>
  <section class="section">
    <div class="columns is-mobile">
      <div
        v-for="(feature, i) of features"
        :key="i"
        class="column">
        <div class="card">
          <header class="card-header">
            <h5 class="card-header-title has-text-grey">{{ feature.title }}</h5>
          </header>
          <div class="card-content">
            <div class="content has-text-centered">
              <p class="content-about">Bsc CSIT stands for Bachelor of science in
                computer science and information technology and designed to provide the student with all sorts of
                knowledge in the field of Information Technology and Computing.
                CSIT is 4 year (8 semester) course of the Institute of Science and Technology, Tribhuvan University. Due
                to emergence of technologies and advancement in every field of the modern world, computer science and
                information technology has become an inevitable part of our life. And it is necessary for everyone to be
                familiar with computer and IT related components. This program develops the skills that are essential
                for both computer professionals and IT specialists. At the completion of this degree, a student will be
                able to design the real world e-media products or create technical solutions to hardware and software
                problems, depending on the chosen area of specialization and electives.
              </p>
              <!--<b-icon-->
              <!--:icon="feature.icon"-->
              <!--size="is-large"-->
              <!--type="is-primary"/>-->
              <ul class="sem-list">
                <li>
                  <a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnb3VFUU4wQkRkbFU?usp=sharing"><h6>Bsc.
                    Csit Semester
                    One</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnSkplQzlJdlh0RFE"><h6>Bsc. Csit Semester
                  Two</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnUmc5Z0VBU0JEZ1E"><h6>Bsc. Csit Semester
                  Three</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnTWh6WWEwTVZ1OFU"><h6>Bsc. Csit Semester
                  Four</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnZENHREQ3WHYyeWM"><h6>Bsc. Csit Semester
                  Fifth</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wnWjN4aFFxcWpnSm8"><h6>Bsc. Csit Semester
                  Sixth</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wndG9Vc3lEOU9hZkk"><h6>Bsc. Csit Semester
                  Seventh</h6></a>
                </li>
                <li><a href="https://drive.google.com/drive/folders/0B9CtJKMoc8wndG9Vc3lEOU9hZkk"><h6>Bsc. Csit Semester
                  Eighth</h6></a>
                </li>
              </ul>
              <p>Let friends know</p>
              <a :href="`https://www.facebook.com/sharer/sharer.php?u=${url}&amp;src=sdkpreparse`"
                 target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24">
                  <path d="M12 0a12 12 0 1 0 0 24 12 12 0 0 0 0-24zm3 8h-1.35c-.54 0-.65.22-.65.78V10h2l-.2 2H13v7h-3v-7H8v-2h2V7.7c0-1.78.93-2.7 3.03-2.7H15v3z"></path>
                </svg>
              </a>
              <a :href="`https://twitter.com/intent/tweet?url=${url};`">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24">
                  <path d="M12 0a12 12 0 1 0 0 24 12 12 0 0 0 0-24zm6.07 9.64A8.12 8.12 0 0 1 9.9 18.2a8.13 8.13 0 0 1-4.4-1.3 5.78 5.78 0 0 0 4.25-1.18 2.88 2.88 0 0 1-2.68-2c.45.09.9.06 1.3-.05a2.88 2.88 0 0 1-2.3-2.85c.38.22.82.35 1.3.36a2.88 2.88 0 0 1-.9-3.83 8.15 8.15 0 0 0 5.92 3 2.88 2.88 0 0 1 4.9-2.62 5.73 5.73 0 0 0 1.82-.7 2.88 2.88 0 0 1-1.26 1.59 5.73 5.73 0 0 0 1.65-.45 5.77 5.77 0 0 1-1.43 1.49z"></path>
                </svg>
              </a>
            </div>
          </div>
          <footer class="card-footer">
            <div class="card-footer-item" v-html="feature.content"></div>
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
          "about": "Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject. Our Vision is to offer pedagogically differentiated technology driven solutions that lead to critical thinking and achievement of higher learning outcomes by seamlessly integrating in-class. Our Aim is to bridge the gap between what is taught in-class using Institutional textbook driven solutions and retail at-home learning providers by seamlessly integrating both. There is no single solution provider offering an end-to-end solution in the market today.",
          "keywords": "shikshalaya Shikshalaya cist CSIT Csit 1st 2nd 3rd 4th 5th 6th 7th 8th first second third fourth fifth sixth seventh eight semester Semester",
          "genre": "Education",
          "datePublished": "2018-09-20",
          "dateCreated": "2018-09-20",
          "dateModified": "2018-09-20",
        },
        features: [
          {
            icon: 'github-circle',
            title: 'Bsc. CIST Books',
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
          'og:title': this.titleTemplate || '',
          'og:description': 'Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject. Our Vision is to offer pedagogically differentiated technology driven solutions that lead to critical thinking and achievement of higher learning outcomes by seamlessly integrating in-class. Our Aim is to bridge the gap between what is taught in-class using Institutional textbook driven solutions and retail at-home learning providers by seamlessly integrating both. There is no single solution provider offering an end-to-end solution in the market today.',
          'og:url': this.url || '',
          'og:image': 'https://cdn.cnn.com/cnnnext/dam/assets/171208142109-03-kalita-books-restricted-exlarge-169.jpg',
          'twitter:title': this.titleTemplate || '',
          'twitter:description': 'Shikshalaya is repository for collection of books, which will eventually help student learn their academic as well as passionate subject. Our Vision is to offer pedagogically differentiated technology driven solutions that lead to critical thinking and achievement of higher learning outcomes by seamlessly integrating in-class. Our Aim is to bridge the gap between what is taught in-class using Institutional textbook driven solutions and retail at-home learning providers by seamlessly integrating both. There is no single solution provider offering an end-to-end solution in the market today.',
          'twitter:url': this.url || '',
          'twitter:image': 'https://cdn.cnn.com/cnnnext/dam/assets/171208142109-03-kalita-books-restricted-exlarge-169.jpg',
        }]
      }
    },
  }
</script>
<style scoped>
  a > h6 {
    color: #a1a2a5;
  }

  ul.sem-list {
    list-style: none;
    text-align: justify;
  }

  .content-about {
    color: #a1a2a5;
    text-align: justify;
  }
</style>
