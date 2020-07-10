<template>
  <div class="content-wrapper bg-background-primary font-sans text-copy-primary leading-normal flex flex-col min-h-screen" :class="theme">
    <header class="border-t-14 border-blue-700">
      <nav class="container mx-auto flex flex-wrap justify-between items-center py-8">
        <div>
          <g-link v-if="theme === 'theme-light'" to="/"><g-image src="../../static/logo.svg" class="w-40" alt="logo" /></g-link>
          <g-link v-else to="/"><g-image src="../../static/logo_dark_mode.svg" class="w-40" alt="logo" /></g-link>
        </div>
        <div class="block lg:hidden">
          <button @click="toggle" class="flex items-center px-3 py-2 border rounded border-gray-500 hover:text-gray-600 hover:border-gray-600">
            <svg class="current-color h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" fill="gray" /></svg>
          </button>
        </div>
        <ul
          class="uppercase tracking-wide font-bold w-full block flex-grow lg:space-x-8 space-y-6 lg:space-y-0 lg:flex lg:flex-initial lg:w-auto items-center mt-8 lg:mt-0"
          :class="isOpen ? 'block': 'hidden'"
        >
          <li class="mb-6 lg:mb-0" v-if="showExtras">
            <search-input />
          </li>
          <li>
            <theme-switcher :theme="theme" @themeChanged="updateTheme" v-if="showExtras" />
          </li>
          <li>
            <a v-if="$route.path === '/'" href="/#notes" v-scroll-to="'#notes'" class="text-copy-primary hover:text-gray-600">Notes</a>
            <g-link v-else to="/#notes" class="text-copy-primary hover:text-gray-600">Notes</g-link>
          </li>
          <li>
            <a v-if="$route.path === '/'" href="/#about" v-scroll-to="'#about'" class="text-copy-primary hover:text-gray-600">About</a>
            <g-link v-else to="/#about" class="text-copy-primary hover:text-gray-600">About</g-link>
          </li>
          <li>
            <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'" class="text-copy-primary hover:text-gray-600">Contact</a>
            <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">Contact</g-link>
          </li>
          <li v-if="showExtras">
            <g-link to="/docs" class="text-copy-primary hover:text-gray-600">Docs</g-link>
          </li>
          <li v-if="showExtras">
            <g-link to="/blog" class="text-copy-primary hover:text-gray-600">Blog</g-link>
          </li>
        </ul>
      </nav>
    </header>

    <div class="flex-grow">
      <slot/>
    </div>
    <footer class="bg-blue-700 text-white">
      <div class="container mx-auto flex flex-col lg:flex-row items-center justify-between py-8">
        <div class="mb-8 lg:mb-0">
          <div>Copyright {{ new Date().getFullYear() }}. All rights reserved.</div>
          <div>
            <a href="/sitemap.xml" class="text-white hover:text-gray-400 font-normal">Sitemap</a>
          </div>
        </div>
        <ul class="flex items-center space-x-8">
          <li>
            <a :href="siteEmail" class="text-white hover:text-gray-400">
              <svg width="25" height="20" fill="currentColor" xmlns="http://www.w3.org/2000/svg"><path d="M2.5 0h20A2.5 2.5 0 0 1 25 2.5v15a2.5 2.5 0 0 1-2.5 2.5h-20A2.5 2.5 0 0 1 0 17.5v-15C0 1.125 1.125 0 2.5 0zm20 4.225V2.5h-20v1.725l10 5 10-5zm0 2.8l-9.438 4.713a1.25 1.25 0 0 1-1.124 0L2.5 7.025V17.5h20V7.025z" fill-rule="nonzero"/></svg>
            </a>
          </li>

          <li>
            <a href="https://www.facebook.com/ktctaxes" target="_blank" class="text-white hover:text-gray-400">
              <svg width="25" height="25" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M400 32H48A48 48 0 0 0 0 80v352a48 48 0 0 0 48 48h137.25V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.27c-30.81 0-40.42 19.12-40.42 38.73V256h68.78l-11 71.69h-57.78V480H400a48 48 0 0 0 48-48V80a48 48 0 0 0-48-48z"/></svg>
            </a>
          </li>

          <li>
            <a href="https://www.linkedin.com/in/kevin-clark-5838757/" target="_blank" class="text-white hover:text-gray-400">
              <svg width="25" height="25" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"/></svg>
            </a>
          </li>

          <li>
            <a href="https://goo.gl/maps/7VtXRggvkDyPb1gg6" target="_blank" class="text-white hover:text-gray-400">
              <svg width="25" height="20" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path d="M288 0c-69.59 0-126 56.41-126 126 0 56.26 82.35 158.8 113.9 196.02 6.39 7.54 17.82 7.54 24.2 0C331.65 284.8 414 182.26 414 126 414 56.41 357.59 0 288 0zm0 168c-23.2 0-42-18.8-42-42s18.8-42 42-42 42 18.8 42 42-18.8 42-42 42zM20.12 215.95A32.006 32.006 0 0 0 0 245.66v250.32c0 11.32 11.43 19.06 21.94 14.86L160 448V214.92c-8.84-15.98-16.07-31.54-21.25-46.42L20.12 215.95zM288 359.67c-14.07 0-27.38-6.18-36.51-16.96-19.66-23.2-40.57-49.62-59.49-76.72v182l192 64V266c-18.92 27.09-39.82 53.52-59.49 76.72-9.13 10.77-22.44 16.95-36.51 16.95zm266.06-198.51L416 224v288l139.88-55.95A31.996 31.996 0 0 0 576 426.34V176.02c0-11.32-11.43-19.06-21.94-14.86z"/></svg>
            </a>
          </li>

        </ul>
      </div>
    </footer>

  </div>
</template>

<script>
import SearchInput from '../components/SearchInput'
import ThemeSwitcher from '../components/ThemeSwitcher'

export default {
  components: {
    SearchInput,
    ThemeSwitcher
  },
  mounted() {
    this.theme = localStorage.getItem('theme') || 'theme-light'
  },
  data() {
    return {
      isOpen: false,
      theme: '',
      siteEmail: 'mailto:' + process.env.GRIDSOME_KTC_EMAIL,
      showExtras: false, // GW Hide Release v2.0 features
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    },
    updateTheme(theme) {
      this.theme = theme
    }
  }
}
</script>

<style src="../css/main.css" />
