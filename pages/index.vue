<template>
  <div>
    <div class="m-8 pt-8">
      <div
        class="bg-gray-100 rounded-md p-2 text-gray-600 md:w-1/4 w-full flex my-2 border-2"
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
        <input
          type="text"
          placeholder="Search using tags"
          class="bg-gray-100 "
          v-model="search"
        />
      </div>

      <div class="md:flex md:justify-between ">
        <div v-for="post in filteredList" :key="post.id">
          <vs-card type="2" class="md:m-2 md:p-2 ">
            <template #title>
              <h3>{{ post.title }}</h3>
            </template>
            <template #img>
              <img :src="`${post.img}`" alt="" />
            </template>
            <template #text>
              <p>
                {{ post.description }}
              </p>
            </template>
            <template #interactions>
              <a
                class="text-muted"
                :href="`https://api.whatsapp.com/send?phone=${post.whatsapp}`"
              >
                <vs-button success>Whatsapp </vs-button></a
              >

              <a class="text-dark" :href="`tel:+${post.phone}`"
                ><vs-button dark>Phone</vs-button></a
              >

              <a
                class="text-dark"
                :href="`https://www.twitter.com/${post.twitter}`"
              >
                <vs-button primary>Twitter</vs-button></a
              >
              <a class="text-dark" :href="`${post.link}`" target="_blank">
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
          <p class="text-sm m-2 p-2">#{{ post.tags }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
class Post {
  constructor(
    id,
    title,
    description,
    link,

    img,
    whatsapp,
    phone,
    twitter,
    tags
  ) {
    this.id = id;
    this.title = title;
    this.description = description;
    this.link = link;

    this.img = img;
    this.whatsapp = whatsapp;
    this.phone = phone;
    this.twitter = twitter;
    this.tags = tags;
  }
}

export default {
  data() {
    return {
      search: "",
      postList: [
        new Post(
          1,
          "Health",
          "Friendship Bench! FREE problem solving therapy with trained community heath workers",
          "https://vuejs.org/",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1620122717/pexels-ali-pazani-2777898_kls9yi.jpg",
          "+263777150345",
          "+263777150345",
          "@CyprianAarons",
          "mentalhealth"
        ),
        new Post(
          2,
          "Health",
          "Friendship Bench! FREE problem solving therapy with trained community heath workers",
          "https://vuejs.org/",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1620122717/pexels-ali-pazani-2777898_kls9yi.jpg",
          "+263777150345",
          "+263777150345",
          "@CyprianAarons",
          "mentalhealth"
        ),
        new Post(
          3,
          "Health",
          "Friendship Bench! FREE problem solving therapy with trained community heath workers",
          "https://vuejs.org/",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1620122717/pexels-ali-pazani-2777898_kls9yi.jpg",
          "+263777150345",
          "+263777150345",
          "@CyprianAarons",
          "health"
        ),
        new Post(
          4,
          "Health",
          "Friendship Bench! FREE problem solving therapy with trained community heath workers",
          "https://vuejs.org/",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1620122717/pexels-ali-pazani-2777898_kls9yi.jpg",
          "+263777150345",
          "+263777150345",
          "@CyprianAarons",
          "marriage"
        )
      ]
    };
  },
  computed: {
    filteredList() {
      return this.postList.filter(post => {
        return post.tags.toLowerCase().includes(this.search.toLowerCase());
      });
    }
  }
};
</script>

<style scoped></style>
