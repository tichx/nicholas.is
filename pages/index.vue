<template>
  <div :class="$style.body">
    <Container :class="{[$style.hidden]: loading}">
      <NavSection name="top" label="" :is-top="true">
        <h1>The world<br>is your oyster,<br>carpe diem!</h1>

        <MoodSet :class="$style.topMoodSet">
          <div slot="left">
            <!-- offset is a percentage of the width of the column. -->
            <MoodImage :scroll-at="1.2"
              src="/mood/nicholas.jpg"
              alt="Nicholas Xu → http://tichx.com"
            />
            <MoodImage :offset="-14" :scroll-at="1.2"
              src="/mood/newyork.jpg"
              alt="January trip to New York city. Nicholas Xu → http://tichx.com"
            />
            <MoodImage :offset="80" :scroll-at="1.2"
              defer-load
              src="/mood/phone.jpg"
              alt="Trip to Los Angeles. Nicholas Xu → http://tichx.com"
            />
            <MoodImage :offset="40" :scroll-at=".9"
              defer-load
              src="/mood/green.jpg"
              alt="Newcastle golf club. Nicholas Xu → http://tichx.com"
            />
          </div>
          <div slot="right">
            <MoodImage :offset="60"
              src="/mood/deer.jpg"
              alt="Found in the Grand Canyon National Park. Nicholas Xu → http://tichx.com"
            />
            <MoodImage orientation="landscape" size="small" :nopin="true"
              src="/mood/Blocky.png"
            />
            <MoodImage orientation="landscape"
              src="/mood/night.jpg"
              alt="My hometown's night view. Nicholas Xu → http://tichx.com"
            />
            <MoodImage :scroll-at="1.1"
              defer-load
              src="/mood/surf.jpg"
              alt="Irvine beach. Nicholas Xu → http://tichx.com"
            />
            <MoodImage orientation="landscape" :offset="20" :scroll-at="1.3"
              defer-load
              src="/mood/singapore.jpg"
              alt="Trip to Singapore with rommate. Nicholas Xu → http://tichx.com"
            />
            <MoodImage orientation="landscape" size="small"  :offset="-30.6" :scroll-at="1.3"
              defer-load
              src="/mood/stamp.png"
            />
          </div>
        </MoodSet>
      </NavSection>

      <NavSection name="bio" label="Bio">
        <vue-marked>
          # Hello.

          I’m Nicholas Xu, a Instagram photographer and an undergrad at the university
          of Washington passionate about computer science. I also travel at least
          few times a year, so may I call my self an experience connoisseur.

          My time are divided by three focuses, school, side projects like this website, and
          photography. I'm currently taking [CSE 143][], [Math 126][], [Arch 151][] this quarter, 
          meet me at the class! I also have done a lot outside of the classroom, founding
          clubs, running small business, etc. I jointly founded a food club, YouFan, with friends last quarter, 
          aiming to connect udub studtents by cooking and sharing delicious cuisine. I also have a
          agency company [Zanke][] that promotes small businesses and individuals on Instagram. 
          It cuts traditional advertisement expenses up to 80% and results showing better engagement
          rate and customer conversion rate.

          I live in Seattle with a plant and coffee. When not frowning at homework, I can be
          found taking photos of [city landscapes][] on [Instagram][] or maybe doing poor latte arts while
          reading Bill Gates's [recommended books][]. 

          [CSE 143]: https://courses.cs.washington.edu/courses/cse143/18wi/
          [Math 126]: https://sites.math.washington.edu/~m126/
          [Arch 151]: https://myplan.uw.edu/Shibboleth.sso/Logout?rd=/student/myplan/course/ARCH151
          [Zanke]: http://zankeapp.com
          [Instagram]: https://www.instagram.com/5.8ft
          [city landscapes]: https://instagram.com/p/BHOK1xlBUOc/
          [recommended books]: hhttps://www.gatesnotes.com/
        </vue-marked>
      </NavSection>
<!--
      <NavSection name="method" label="Methodology" :numbered-headings="true">
        <vue-marked>
          ## People, not users

          The infinite parade of glowing rectangles can cloud our view, but
          products are in service of people. Human connection is the best cure
          for our assumptions. Curiosity and empathy build bridges—fueling the
          research and synthesis that are core to great product design.

          ## Begin at the end

          Great endings inspire great beginnings. What will your legacy be?
          Will you proudly sign your name? Crystallizing the outcome enables us
          to define how to achieve it, measure progress, and anticipate many of
          the changing conditions to come.

          ## Maker’s vault

          When it comes to making, processes vary greatly. One constant is the
          need for large blocks of uninterrupted time to focus. In an
          increasingly open environment with diverse disciplines, establishing
          clear boundaries leads to fruitful outcomes and happy teams.

          ## Co-lab

          Iterative feedback and collaboration directly equate to product
          quality. Ask hard questions, find the holes, swap files, and gain new
          perspectives. Use prototyping and testing to address issues early on
          and illuminate new opportunities.

          ## Redefine the bar

          Product design is an endless negotiation of necessary compromises,
          but constraints never deter the ingenious. A dedication to craft and
          relentless commitment to differentiate produce not just great, but
          groundbreaking results.

          ## Onwards and upwards

          Reflection is the ultimate catalyst for growth. Retrospectives,
          coaching, one-on-ones, and time budgeted for introspection are
          ingredients essential to perpetual development. The best product
          teams prioritize learning from experience, and everyone benefits.
        </vue-marked>
      </NavSection>

      <NavSection name="case-studies" label="Case Studies">
        <vue-marked>
          # Airbnb:
          # Scaling the Heart

          Building the Design Language System powering Airbnb innovation.
        </vue-marked>

        <ImageViewer defer-load :images="[
          {src: '/airbnb/Airbnb-MMXV.jpg', alt: 'Airbnb MMXV. Nicholas Xu → http://tichx.com'},
          ]" />

        <vue-marked>
          In January of 2015, I joined Airbnb. While the design team of 20 that
          could fit snugly around a whiteboard would quadruple before my
          departure less than a year and a half later, a signature climate of
          warmth never faltered.

          Up until this point, Airbnb had grown organically. The widely
          publicized rebrand six months prior had catapulted an
          already-valuable service into the “internet darling” stratosphere.
          2015 would usher in the company’s first significant investment in
          global marketing, further extending its reach. Internally, teams
          were working and growing at a feverish pace.

          By July, product design had more than doubled in size. Teams and
          initiatives across the org struggled to stay in sync. Web, iOS,
          Android, and Watch each had unique designs and codebases. We needed a
          shared language and a stable and performant foundation to withstand
          continued growth.

          Our goal was to create a universal design system and I was given the
          green light to build a dedicated team.
        </vue-marked>

        <ImageViewer defer-load :images="[
          {src: '/airbnb/Airbnb-DLS-Founding-Team.jpg', alt: 'Airbnb Design Systems Team. Salih Abdul-Karim, Bek Stone, Michael Sui, Jing Jian. https://bek.is'},
          ]" />

        <vue-marked>
          As the founding members began to research and audit, I set out to
          connect with leaders across the organization to gain understanding,
          exchange ideas, and develop shared goals for our future. Armed with
          insights, I drafted our first vision and guiding principles and set
          the growing team loose to explore and create.

          Fonts would be scaled up for legibility. Color contrast boosted to
          meet new accessibility benchmarks. Bold accents introduced pacing and
          illustrations rang harmonious with our expanding icon system.
          Movement brought life. A visual language emerged—vibrant, clear, and
          as animated and conversational as the dinner table.
        </vue-marked>

        <MoodSet>
          <div slot="left">
            <MoodImage
              defer-load
              src="/airbnb/Type-Scales.jpg"
              alt="Airbnb type scales by Britt Nelson. Nicholas Xu → http://tichx.com"
              :scroll-at="1.2"
              :offset="80" />
            <MoodImage
              defer-load
              src="/airbnb/DLS-Pacing.png"
              alt="Airbnb app component system. Nicholas Xu → http://tichx.com"
              orientation="landscape"
              :scroll-at="1.2"
              :offset="-10" />
          </div>
          <div slot="right">
            <MoodImage
              defer-load
              src="/airbnb/Airbnb-DLS-Brand.jpg"
              alt="Airbnb Design Systems team. Michael Sui, Britt Nelson, Jing Jian. Nicholas Xu → http://tichx.com"
              orientation="landscape"
              :scroll-at="0.9"
              :offset="10" />
            <MoodImage
              defer-load
              src="/airbnb/DLS-Calendar.png"
              alt="Airbnb app date picker. Nicholas Xu → http://tichx.com"
              :scroll-at="1.1"
              :offset="0" />
            <MoodImage
              defer-load
              src="/airbnb/DLS-Motion.gif"
              alt="Airbnb in motion. https://bek.is"
              orientation="landscape"
              size="small"
              :scroll-at="1"
              :offset="40" />
          </div>
        </MoodSet>

        <vue-marked>
          Running in parallel were two initiatives introducing radical changes
          to flows across all platforms. The success of these colossal efforts
          hinged on having a sound and iconic system to build upon. Quality
          cannot be defined by external characteristics alone. Reliability and
          performance are inextricable traits, and required tremendous
          cooperation across product, engineering, and design to achieve. We
          focused our efforts on mobile to lead the way.
        </vue-marked>

        <ImageViewer defer-load :images="[
          {src: '/airbnb/Airbnb-DLS-Leads.jpg', alt: 'Airbnb Design Language System. Alex Schleifer, Bek Stone, Amber Cartwright, Adam Michela. https://bek.is'},
          {src: '/airbnb/Airbnb-DLS.jpg', alt: 'Airbnb Design Language System. Brian Chesky, Joe Zadeh, Alex Schleifer, Bek Stone, Amber Cartwright. https://bek.is'},
          {src: '/airbnb/Airbnb-DLS-Components.jpg', alt: 'Airbnb Design Language System. Alex Schleifer, Bek Stone, Amber Cartwright. https://bek.is'},
          ]" />

        <vue-marked>
          Equipped with new requirements and our drafted brand
          language, design leads and executives from our cross-functional teams
          headed offsite to hash out the first version of Airbnb’s Design
          Language System. Teams began testing, breaking, and submitting
          improvements. As the system solidified, I guided adoption,
          integration, and continued evolution across product teams.
        </vue-marked>

        <FramedVideo
          src="https://s3.us-west-2.amazonaws.com/bek-is/Airbnb-DLS-Components-Demo.mp4"
          defer-load
          poster="/airbnb/Loading.gif"
        />

        <vue-marked>
          As with any great endeavor, this one too had to travel the difficult
          but transformative path of discovery. No one solution could meet all
          needs, and no process could satisfy all those involved. More valuable
          than the system created were the people it aimed to serve. At last, a
          shared language was beginning to bridge the gap between disciplines,
          and something altogether more beautiful was unfolding.

          With the rollout underway and an able team in place, I departed from
          Airbnb—one month before the public launch in April, 2016. The team
          and their work continue to flourish, driving a greater level of
          continuity and cross-functional collaboration.

          Laying a new foundation and rebuilding a home with a growing family
          inside was no small feat, and there were countless challenges and
          opportunities for the organization to learn along the way. In the
          end, a once small and mighty team empowered Airbnb to scale in new
          ways—each step more humane than the last.
        </vue-marked>

        <MoodSet>
          <div slot="left">
            <MoodImage
              defer-load
              src="/airbnb/Airbnb-2015-XD.jpg"
              alt="2015 Airbnb design team. Nicholas Xu → http://tichx.com"
              :scroll-at="1.2"
              :offset="80" />
            <MoodImage
              defer-load
              src="/airbnb/Karri-Saarinen.jpg"
              alt="Karri Saarinen in Wintercroft mask. https://wintercroft.com/"
              orientation="landscape"
              :scroll-at="1.2"
              :offset="-10" />
          </div>
          <div slot="right">
            <MoodImage
              defer-load
              src="/airbnb/Airbnb-FutureIsFemale.jpg"
              alt="EPIC / Airbnb. Katie Dill, Bek Stone, Amber Cartwright. https://bek.is"
              orientation="landscape"
              :scroll-at="1.1" />
            <MoodImage
              defer-load
              src="/airbnb/SalihTheDream.jpg"
              alt="Salih Abdul-Karim, master of motion."
              :scroll-at="0.9"
              :offset="-10" />
            <MoodImage
              defer-load
              src="/airbnb/HowWeBuild.jpg"
              alt="Airbnb design team. Nicholas Xu → http://tichx.com"
              orientation="landscape"
              :offset="60" />
          </div>
        </MoodSet>

        <vue-marked>
          ## Encore

          Core contributors:  
          Alex Schleifer, Adam Michela, Karri Saarinen, Michael Bachand, Paul
          Kompfner, Sean Abraham, Salih Abdul-Karim, Michael Sui, Jing Jian,
          Britt Nelson, Hannah Hughes, Luke Carter, Stephen Wyatt Bush.

          Invaluable partners:  
          Katie Dill, Amber Cartwright, Allen Mask, Taido Nakajima, Katie Chen,
          Adam Glynn-Finnegan, Kevin Grennan, Alvin Hsia, Shane Allen, Charlie
          Aufmann.
          
          ## Related articles

          [A Design System to Take on the World](http://www.creativebloq.com/features/why-design-is-key-to-airbnbs-incredible-success)  
          *by Tanya Combrinck*

          [The Way We Build](https://airbnb.design/the-way-we-build/)  
          *by Alex Schleifer*

          [Creating the Airbnb Design System](http://karrisaarinen.com/posts/building-airbnb-design-system/)  
          *by Karri Saarinen*

          [Communicating Clarity and Charm](https://design.google/library/airbnb-communicating-clarity-and-charm/)  
          *by Google Design*
        </vue-marked>
      </NavSection>

      <NavSection name="archives" label="Archives">
        <vue-marked>
          # Making and breaking

          Highlights from humanizing brands and digital experiences,
          constructing environments, and exploring physical forms and
          materials.
        </vue-marked>

        <ImageViewer defer-load :images="[
          {src: '/archive/BekStone-CastSilver.jpg', alt: 'Cast silver. Nicholas Xu → http://tichx.com'},
          {src: '/archive/Constellations.jpg', alt: 'Constellations journal. Nicholas Xu → http://tichx.com'},
          {src: '/archive/Emboss.jpg', alt: 'TLE branding. Nicholas Xu → http://tichx.com'},
          {src: '/archive/Flytrap-Construction.jpg', alt: 'Making and breaking at the Flytrap. Nicholas Xu → http://tichx.com'},
          {src: '/archive/Goflow-App.jpg', alt: 'Goflow app design, icon and component system. Nicholas Xu → http://tichx.com'},
          {src: '/archive/NEU.jpg', alt: 'New Engineering University. Nicholas Xu → http://tichx.com'},
          {src: '/archive/PressedJuicery.jpg', alt: 'Pressed Juicery branding. Nicholas Xu → http://tichx.com'},
          {src: '/archive/TLE-3D-Mark.jpg', alt: '3D mark. Nicholas Xu → http://tichx.com'},
          {src: '/archive/ThisIsBound.jpg', alt: 'Leatherworking. Nicholas Xu → http://tichx.com'},
          {src: '/archive/Workshop.jpg', alt: 'Technical apparel design. Nicholas Xu → http://tichx.com'},
          ]" />
      </NavSection>

      <NavSection name="voices" label="Voices">
        <vue-marked>
          > Bek is one of those rare leaders that boldly balances hands-on
          > relevancy with clear visioned execution.

          [Ryan Northway](https://www.linkedin.com/in/northway/)  
          *Principal Product Designer, Real Labs*

          > A shining star in a sea of sameness, an invigorator, an
          > inspiration.

          [Benjamin Roy](https://www.linkedin.com/in/beroy/)  
          *Director, Venture Visuals*

          > An expert in her craft, a leader with humility, and someone you can
          > always rely on to deliver innovative and fresh design perspectives.

          [Adam Bordow](https://www.linkedin.com/in/adam-bordow-a513557/)  
          *Photo Editor, Airbnb*

          > If I could get Bek on my team ever again I'd do so in a heartbeat.

          [Dan Hill](https://www.linkedin.com/in/hilldan/)  
          *Director of Product, Airbnb*
        </vue-marked>
      </NavSection>
-->
      <NavSection name="" label="Connect" :nav-hidden="true">
        <Contact />
      </NavSection>
    </Container>

    <Splash />
    <NavMenu />
  </div>
</template>

<style lang="stylus" module>
  @require '~assets/util'

  // Keep NavMenu stacking above contents, but display first.
  .body
    display flex
    flex-direction column-reverse

  .hidden
    visibility hidden

  .top-mood-set
    padding-bottom 90px
    +below(tablet)
      margin-top 100px
    +above(tablet)
      margin-top 180px
</style>

<script>
import {mapMutations, mapState} from 'vuex';

import Contact from '~/components/Contact.vue';
import Container from '~/components/Container.vue';
import FramedVideo from '~/components/FramedVideo.vue';
import ImageViewer from '~/components/ImageViewer.vue';
import MoodImage from '~/components/MoodImage.vue';
import MoodSet from '~/components/MoodSet.vue';
import NavMenu from '~/components/NavMenu.vue';
import NavSection from '~/components/NavSection.vue';
import Splash from '~/components/Splash.vue';
import VueMarked from 'vue-marked';

export default {
  components: {
    Contact,
    Container,
    FramedVideo,
    ImageViewer,
    MoodImage,
    MoodSet,
    NavMenu,
    NavSection,
    Splash,
    VueMarked,
  },

  computed: mapState(['loading']),

  methods: {
    onScroll() {
      this.setScrollY(window.scrollY);
    },

    ...mapMutations(['setScrollY']),
  },

  mounted() {
    window.addEventListener('scroll', this.onScroll, false);
  },

  destroyed() {
    window.removeEventListener('scroll', this.onScroll);
  },
};
</script>
