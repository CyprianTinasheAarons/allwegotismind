<template>
  <div>
    <div class="m-8 pt-8">
      <div
        class="bg-gray-100 rounded-md p-2 text-gray-600 md:w-1/4 w-full flex m-2 p-2 "
      >
        <svg
          class="w-6 h-6"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
            clip-rule="evenodd"
          ></path>
        </svg>
        <input type="text" placeholder="Search site..." class="bg-gray-100" />
      </div>
      <div class="md:flex md:justify-between ">
        <div class="md:flex md:justify-between ">
          <div v-for="i in 4" :key="i">
            <vs-card type="2" class="m-2 p-2 ">
              <template #title>
                <h3>Friendship Bench</h3>
              </template>
              <template #img>
                <img
                  src="../static/pexels-rodnae-productions-6936081.jpg"
                  alt=""
                />
              </template>
              <template #text>
                <p>
                  Friendship Bench! FREE problem solving therapy with trained
                  community heath workers.
                </p>
              </template>
              <template #interactions>
                <a
                  class="text-muted"
                  href="https://api.whatsapp.com/send?phone=263777150345"
                >
                  <vs-button success>Whatsapp </vs-button></a
                >

                <a class="text-dark" href="tel:+263777150345"
                  ><vs-button dark>Phone</vs-button></a
                >

                <a
                  class="text-dark"
                  href="https://www.twitter.com/allwegotismind"
                >
                  <vs-button primary>Twitter</vs-button></a
                >
                <a
                  class="text-dark"
                  href="https://allwegotismind.netlify.app"
                  target="_blank"
                >
                  <vs-button style="background-color:#519657;"
                    ><svg
                      class="w-6 h-6"
                      fill="currentColor"
                      viewBox="0 0 20 20"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"
                      ></path>
                      <path
                        d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"
                      ></path></svg
                  ></vs-button>
                </a>
              </template>
            </vs-card>
            <p class="text-sm">#Mental #Doctor #Health</p>
          </div>
        </div>
      </div>
      <div class="md:flex md:justify-between ">
        <div v-for="i in 4" :key="i">
          <vs-card type="2" class="m-2 p-2 ">
            <template #title>
              <h3>Friendship Bench</h3>
            </template>
            <template #img>
              <img
                src="../static/pexels-rodnae-productions-6936081.jpg"
                alt=""
              />
            </template>
            <template #text>
              <p>
                Friendship Bench! FREE problem solving therapy with trained
                community heath workers.
              </p>
            </template>
            <template #interactions>
              <a
                class="text-muted"
                href="https://api.whatsapp.com/send?phone=263777150345"
              >
                <vs-button success>Whatsapp </vs-button></a
              >

              <a class="text-dark" href="tel:+263777150345"
                ><vs-button dark>Phone</vs-button></a
              >

              <a
                class="text-dark"
                href="https://www.twitter.com/allwegotismind"
              >
                <vs-button primary>Twitter</vs-button></a
              >
              <a
                class="text-dark"
                href="https://allwegotismind.netlify.app"
                target="_blank"
              >
                <vs-button style="background-color:#519657;"
                  ><svg
                    class="w-6 h-6"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"
                    ></path>
                    <path
                      d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"
                    ></path></svg
                ></vs-button>
              </a>
            </template>
          </vs-card>
          <p class="text-sm">#Mental #Doctor #Health</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped></style>
