<template>
  <div class="flex flex-col min-h-screen">
    <template>
      <div class="md:block hidden">
        <vs-navbar not-line center-collapsed v-model="active">
          <template #left>
            <h1 class="tracking-wider uppercase font-semibold">
              🧠 AllWeGotIsMind
            </h1>
          </template>
          <template #right>
            <vs-navbar-item :active="active == 'list'" id="list">
              <a
                href="https://form.jotform.com/211375284893060"
                target="_blank"
              >
                Join List</a
              >
            </vs-navbar-item>
            <vs-navbar-item :active="active == 'blog'" id="blog">
              <a href="https://medium.com/@allwegotismind" target="_blank">
                Blog</a
              >
            </vs-navbar-item>
          </template>
        </vs-navbar>
      </div>
    </template>
    <template>
      <div class="flex justify-between items-center md:hidden block">
        <button @click="openMenu">
          <svg
            class="w-12 h-12 m-2"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
              clip-rule="evenodd"
            ></path>
          </svg>
        </button>

        <div class="flex  m-2">
          <h1 class="tracking-wider uppercase font-semibold">
            🧠 AllWeGotIsMind
          </h1>
        </div>
      </div>
    </template>
    <template>
      <div class="md:hidden block " v-if="sideNavbarVisible">
        <vs-sidebar absolute v-model="active" open>
          <template #logo>
            <h1 class="tracking-wider uppercase font-semibold">
              🧠 AllWeGotIsMind
            </h1>
            <button @click="closeMenu">
              <svg
                class=" mx-2 w-12 h-12"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </button>
          </template>

          <vs-sidebar-item id="list">
            <a href="https://form.jotform.com/211375284893060" target="_blank">
              😁 Join List</a
            >
          </vs-sidebar-item>
          <vs-sidebar-item id="list">
            <a href="https://medium.com/@allwegotismind" target="_blank">
              📕 Blog</a
            >
          </vs-sidebar-item>
        </vs-sidebar>
      </div>
    </template>

    <Nuxt class="flex-grow" />
    <footer class="text-gray-600 body-font ">
      <div class="border m-4 p-4 rounded">
        <p>
          <span class="font-semibold">😉 Disclaimer: </span> information
          provided on this website does not, and is not intended to, constitute
          medical advice; instead, all information, content, and materials
          available on this site are for general informational purposes only.
          This website contains links to other third-party websites. Such links
          are only for the convenience of the user and we are not responsible
          for them.
        </p>
      </div>
      <div class="bg-gray-100">
        <div
          class="container px-5 py-6 mx-auto flex items-center sm:flex-row flex-col"
        >
          <a
            class="flex title-font font-medium items-center md:justify-start justify-center text-gray-900"
          >
            <h1 class="tracking-wider uppercase font-semibold">
              🧠 AllWeGotIsMind
            </h1>
          </a>
          <p class="text-sm text-gray-500 sm:ml-6 sm:mt-0 mt-4">
            © {{ new Date().getFullYear() }} AllWeGotIsMind —
            <a
              href="https://twitter.com/cyprianaarons"
              rel="noopener noreferrer"
              class="text-gray-600 ml-1"
              target="_blank"
              >@cyprianaarons</a
            >
          </p>
          <span
            class="inline-flex sm:ml-auto sm:mt-0 mt-4 justify-center sm:justify-start"
          >
            <a
              class="text-gray-500"
              href="https://www.facebook.com/allwegotismind"
              target="_blank"
            >
              <svg
                fill="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-5 h-5"
                viewBox="0 0 24 24"
              >
                <path
                  d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"
                ></path>
              </svg>
            </a>
            <a
              class="ml-3 text-gray-500"
              href="https://twitter.com/CyprianAarons"
              target="_blank"
            >
              <svg
                fill="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-5 h-5"
                viewBox="0 0 24 24"
              >
                <path
                  d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"
                ></path>
              </svg>
            </a>
            <a
              class="ml-3 text-gray-500"
              href="https://www.instagram.com/allwegotis"
              target="_blank"
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-5 h-5"
                viewBox="0 0 24 24"
              >
                <rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
                <path
                  d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37zm1.5-4.87h.01"
                ></path>
              </svg>
            </a>
          </span>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: "home",
      sideNavbarVisible: false
    };
  },
  components: {},
  methods: {
    openMenu() {
      this.sideNavbarVisible = true;
      document.documentElement.style.overflow = "hidden";
    },

    closeMenu() {
      this.sideNavbarVisible = false;
      document.documentElement.style.overflow = "auto";
    }
  }
};
</script>
