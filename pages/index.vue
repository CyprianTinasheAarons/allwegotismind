<template>
  <div>
    <div class="m-8 pt-8">
      <div class="md:flex md:justify-between ">
        <vs-card type="2" v-for="i in 4" :key="i" class="m-2 p-2 sm:w-full">
          <template #title>
            <h3>Friendship Bench</h3>
          </template>
          <template #img>
            <img src="../static/pexels-rodnae-productions-6936081.jpg" alt="" />
          </template>
          <template #text>
            <p>
              Friendship Bench! FREE problem solving therapy with trained
              community heath workers.
            </p>
          </template>
          <template #interactions>
            <vs-button success>Whatsapp </vs-button>
            <vs-button primary>Twitter</vs-button>
            <vs-button dark>Phone</vs-button>
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
          </template>
        </vs-card>
      </div>
      <div class="md:flex md:justify-between ">
        <vs-card type="2" v-for="i in 4" :key="i" class="m-2 p-2 ">
          <template #title>
            <h3>Friendship Bench</h3>
          </template>
          <template #img>
            <img src="../static/pexels-rodnae-productions-6936081.jpg" alt="" />
          </template>
          <template #text>
            <p>
              Friendship Bench! FREE problem solving therapy with trained
              community heath workers.
            </p>
          </template>
          <template #interactions>
            <vs-button success>Whatsapp </vs-button>
            <vs-button primary>Twitter</vs-button>
            <vs-button dark>Phone</vs-button>
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
          </template>
        </vs-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped></style>
