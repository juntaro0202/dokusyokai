<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/STOCKER1202116.jpg')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .8), rgba(5, 11, 31, .8)"
      max-height="100"
    >
      <v-container class="fill-height px-4 py-12">
        <v-responsive
          class="d-flex align-center"
          height="100%"
          max-width="700"
          width="100%"
        >
          <base-heading
            title="読書は一人でするのではなく、対話を通して行うもの"
          />

          <base-body>
            <p>本サイトは我々の人生に大いに役立つ書籍を使い、</p>
            <p>自分自身の思考を一段深めるきっかけを作ることを目的とした</p>
            <p>読書会に関する情報を提供するサイトです。</p>
          </base-body>

          <div
            :class="
              $vuetify.breakpoint.smAndDown
                ? 'flex-column align-start'
                : 'align-center'
            "
            class="d-flex flex-wrap"
          >
            <base-btn> 登録はこちら </base-btn>

            <span class="font-weight-bold ml-6 mr-4 my-4">or</span>

            <base-btn :ripple="false" class="pa-1" height="auto" text>
              既に会員の方のログインはこちら
            </base-btn>
          </div>
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
export default {
  name: "SectionHero",

  provide: {
    theme: { isDark: true },
  },

  computed: {
    minHeight() {
      const height = this.$vuetify.breakpoint.mdAndUp ? "100vh" : "50vh";

      return `calc(${height} - ${this.$vuetify.application.top}px)`;
    },
  },
};
</script>
