<template>
  <div>
    <v-carousel cycle height="650" hide-delimiter-background :show-arrows="false">
      <v-carousel-item v-for="item in news" :key="item.id">
        <img width="100%" :src="item.full_image" alt="" />
      </v-carousel-item>
    </v-carousel>
    <h2 class="mt-5 text-center">Новостной портал Шлёпа News</h2>
    <h3 class="mt-5 text-center" >Только базированные новости от проверенных источников!</h3>
    <h4 class="mt-5 text-center">Если ты не веришь большому русскому коту, то что-то в твоей жизни не так. Кот - база. Не кот - кринж. Запомни.</h4>
  </div>
</template>

<script>
  export default {
    name: "IndexPage",
    computed: {
      news() {
        return this.$store.getters.getListNews
      },
    },
  }
</script>
