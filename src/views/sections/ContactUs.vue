<template>
  <v-theme-provider dark>
    <base-section id="contact-us" class="primary" space="40">
      <v-container>
        <v-row justify="center">
          <v-col cols="10">
            <base-title
              :space="$vuetify.breakpoint.mdAndUp ? 0 : 4"
              title="お問い合わせ等はこちらからお願いします。"
            />

            <base-body space="0">
              <span class="white--text">
                内容を確認の上、48時間以内を目処に ご回答を差し上げます。
              </span>
            </base-body>
          </v-col>

          <v-col cols="12" md="2">
            <base-btn
              :block="$vuetify.breakpoint.smAndDown"
              color="white"
              href="mailto:shop@vuetifyjs.com?subject=Zero%20Theme%20Question"
              large
              outlined
              target="_blank"
            >
              Contact Us
            </base-btn>
          </v-col>
        </v-row>
      </v-container>
    </base-section>
  </v-theme-provider>
</template>

<script>
export default {
  name: "SectionContactUs",
};
</script>
