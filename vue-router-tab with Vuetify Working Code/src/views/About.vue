/* eslint-disable prettier/prettier */
<template>
  <div class="about">
    <h1>This is an about page</h1>

    <v-row class="mx-0">
      <v-col cols="3">
          <div class="greybox rounded text-center">
            <v-row class="d-flex align-items-center justify-center">
              <div class="textLg">This is some text </div>
              <div class="textLg circlebg">Covid 19</div>
            </v-row>
          </div>
      </v-col>

      <v-col cols="3">
          <div class="greybox rounded text-center">
                <v-btn
                  dark
                  color="red darken-2"
                  @click="snackbar = true"
                >
                  Open Snackbar
                </v-btn>

                <v-snackbar
                  v-model="snackbar"
                  :multi-line="multiLine"
                >
                  {{ text }}
                  <v-btn
                    color="red"
                    text
                    @click="snackbar = false"
                  >
                    Close
                  </v-btn>
                </v-snackbar>
          </div>
      </v-col>

    </v-row>

  </div>
</template>
<script>
  export default {
    data: () => ({
      multiLine: true,
      snackbar: false,
      text: 'I\'m a multi-line snackbar.',
    }),
  }
</script>

<style lang="scss" scoped>
.about {
  text-align: center;
}
</style>
