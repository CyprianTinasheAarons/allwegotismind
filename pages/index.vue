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
            <vs-button danger icon>Whatsapp </vs-button>
            <vs-button danger icon>Twitter</vs-button>
            <vs-button danger icon>Phone</vs-button>
            <vs-button danger icon>Site</vs-button>
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
            <vs-button danger icon>Whatsapp </vs-button>
            <vs-button danger icon>Twitter</vs-button>
            <vs-button danger icon>Phone</vs-button>
            <vs-button danger icon>Site</vs-button>
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
