<template>
  <div class="bg-gray-100">
    <div class="m-8 pt-8">
      <div
        class="bg-gray-100 rounded-md p-2 text-gray-600 md:w-1/4 w-full flex my-2 md:mx-4 border-2"
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
          placeholder="Search using title"
          class="bg-gray-100 "
          v-model="search"
        />
      </div>

      <div class="md:flex md:justify-between " v-if="posts.length">
        <div v-for="(chunk, index) in posts" :key="index">
          <div v-for="post in chunk" :key="post.id">
            <vs-card type="3" class="md:m-2 md:p-2   ">
              <template #title>
                <h3>{{ post.title }}</h3>
              </template>
              <!-- <template #img>
                <img
                  :src="`${post.img}`"
                  alt="image"
                  class="h-48 w-32 object-cover"
                />
              </template> -->
              <template #text>
                <p class="py-2">
                  {{ post.description }}
                </p>
                <div class="flex justify-around">
                  <a
                    class="text-muted"
                    :href="
                      `https://api.whatsapp.com/send?phone=${post.whatsapp}`
                    "
                    v-if="post.whatsapp"
                  >
                    <vs-button style="background-color:#eee">
                      <img
                        src="../static/whatsapp-svgrepo-com.svg"
                        class="w-6 h-6"
                      /> </vs-button
                  ></a>

                  <a
                    class="text-dark"
                    :href="`tel:${post.phone}`"
                    v-if="post.phone"
                    ><vs-button style="background-color:#607d8b"
                      ><svg
                        class="w-6 h-6"
                        fill="currentColor"
                        viewBox="0 0 20 20"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
                        ></path></svg></vs-button
                  ></a>

                  <a
                    class="text-dark"
                    :href="`https://www.twitter.com/${post.twitter}`"
                    v-if="post.twitter"
                  >
                    <vs-button style="background-color:#eee">
                      <img
                        src="../static/twitter-svgrepo-com.svg"
                        class="w-6 h-6"
                      /> </vs-button
                  ></a>
                  <a
                    class="text-dark"
                    :href="`${post.link}`"
                    v-if="post.link"
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
                </div>
              </template>
            </vs-card>
            <div class="flex ">
              <p
                class="text-xs mx-1 p-1 text-gray-500"
                v-for="(tag, index) in post.tags"
                :key="index"
              >
                #{{ tag }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <div v-else>
        <div class="flex justify-around">
          <img
            src="../static/undraw_sunlight_tn7t.svg"
            class="object-cover md:w-1/4 w-full"
          />
        </div>
        <h1 class="text-center font-semibold md:text-3xl text-xl m-2 p-2">
          Sorry we didn't get anything.😊 But you can always try again. LOL
        </h1>
      </div>
    </div>
  </div>
</template>

<script>
import _ from "lodash";

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
          "The Friendship Bench",
          "Friendship Bench! FREE problem solving therapy with trained community heath workers",
          "https://friendshipbenchzimbabwe.org",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621891869/1589946087441_k49h3i.jpg",
          "+263784845294",
          "+263784845294",
          "@friendshipbench",
          ["friends", "free", "therapy"]
        ),
        new Post(
          2,
          "Phoebe Zimbabwe",
          "PHOEBE Zimbabwe - focuses on gender based advocacy catering for women in vulnerable situations. ",
          "https://phoebecentre.org.uk/zimbabwe/",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621892532/phoebe_dcu3b9.png",
          "+263714396012",
          "+263714396012",
          "@PhoebeZimbabwe",
          ["gender", "women"]
        ),
        new Post(
          3,
          "Christian Counseling Center",
          "Christian Counseling Center - you don’t need to be a Christian or religious in any regard to seek help here. ",
          "https://christiancounsellingcentre.net",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621892650/Christian_iaoico.jpg",
          "+263773547544",
          "+263773547544",
          "",
          ["counseling", "religious", "christian"]
        ),
        new Post(
          4,
          "Create Zim",
          "Create Zim - A platform for youths to connect and use their talents recreationally. Offers mindfulness workshops and free consultations with professionals.",
          "",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621891956/create_zim_sz0i9q.png",
          "+263772634466",
          "+263772634466",
          "@create_zim", //On IG
          ["counselling", "workshops", "mindfulness"]
        ),
        new Post(
          5,
          "Connect Zimbabwe",
          "Connect Zimbabwe Institute of Systemic Therapy - their objective is to provide counselling and therapeutic services for individuals, families and communities to overcome a wide variety of social challenges",
          "https://connect.co.zw",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621892720/connect_atg7kl.png",
          "+263778914501",
          "+263713 794 846",
          "",
          ["therapy", "families", "communities"]
        ),
        new Post(
          6,
          "Unearthed ZW",
          "Unearthed ZW - a space to bring together those suffering from depression",
          "",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621893555/unearthed_xmdyna.png",
          "+263774058764",
          "+263774058764",
          "",
          ["support", "depression"]
        ),
        new Post(
          7,
          "Musasa Project",
          "Musasa Project - an NGO whose operations are based on advocacy, peace building and provision of direct  services such as counselling, legal aid, medical assistance, life skills and temporary shelter  to survivors of GBV",
          "https://musasa.co.zw",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621892405/musasa_modfmq.webp",
          "+2638080074",
          "+2637754423000",
          "",
          ["medical", "counseling", "GBV"]
        ),
        new Post(
          8,
          "Xoxa",
          "Xoxa - the first Mental Wellness chat app of its kind in Zimbabwe. You can chat to volunteers between 9am and 9pm about pretty much anything.",
          "https://xoxa.co.zw",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621892971/Screenshot_2021-05-24_at_23.49.19_etjrbp.png",
          "",
          "",
          "",
          ["health", "mental", "wellness"]
        ),
        new Post(
          9,
          "Africa Open Up",
          " Africa open up - a space for teenagers to talk about things they may not be comfortable telling their parents or who have parents who work a lot and don’t have the time to talk",
          "https://meetafricaopenup.wixsite.com/open ",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621893190/Screenshot_2021-05-24_at_23.53.02_c85hfg.png",
          "+263777791626",
          "+263777791626",
          "@AfricansUp",
          ["parents", "teenagers"]
        ),
        new Post(
          10,
          "Zimbabwe OCD Trust",
          " Zimbabwe OCD trust - Raises awareness and provides support to individuals and Zimbabwean communities who suffer from OCD and anxiety disorders.",
          "https://zimbabweocdtrust.org/take-action",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621893241/Zim_OCD_trust_sllm8k.png",
          "+263772298286",
          "+263772298286",
          "",
          ["health", "mental", "youth"]
        ),
        new Post(
          11,
          "Global Institute of Emotional Health",
          "Global Institute of Emotional Health and Wellness - helps people achieve mental and emotional well-being through innovative platforms that are accessible and free",
          "https://mentalhealthsa.org.za",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621893322/GlobalInstituteOfEmotionalHealthWellness_LogoDesignFINAL_JPG-500x353_pg2yqf.jpg",
          "+263778914501",
          "+263713794846",
          "@create_zim",
          ["emotional", "mental", "free"]
        ),
        new Post(
          12,
          "Wellnesshub",
          "Connect Zimbabwe Institute of Systemic Therapy - their objective is to provide counselling and therapeutic services for individuals, families and communities to overcome a wide variety of social challenges",
          "https://wellnesshub.co.zw",
          "https://res.cloudinary.com/dqzpz4w3l/image/upload/v1621893430/WIK8BboF_400x400_q1ctet.jpg",
          "+2638080475",
          "",
          "@WellnessHub_Zim",
          ["families", "counseling", "challenges"]
        )
      ]
    };
  },
  computed: {
    filteredList() {
      return this.postList.filter(post => {
        return this.search.length > 2
          ? post.title
              .toLowerCase()
              .trim()
              .includes(this.search.toLowerCase().trim())
          : post;
      });
    },
    posts() {
      return _.chunk(Object.values(this.filteredList), 3);
    }
  }
};
</script>

<style scoped></style>
