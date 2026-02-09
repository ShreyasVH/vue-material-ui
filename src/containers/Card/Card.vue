<template>
  <div style="height: 1000px">
    <v-card
        class="mx-auto"
        max-width="344"
    >
      <v-card-text>
        <div>Word of the Day</div>

        <p class="text-h4 font-weight-black">el·ee·mos·y·nar·y</p>

        <p>adjective</p>

        <div class="text-medium-emphasis">
          relating to or dependent on charity; charitable; charitable donations. Pertaining to alms.<br>
          "an eleemosynary educational institution."
        </div>
      </v-card-text>

      <v-card-actions>
        <v-btn
            color="teal-accent-4"
            text="Learn More"
            variant="text"
            @click="reveal = true"
        ></v-btn>
      </v-card-actions>

      <v-expand-transition>
        <v-card
            v-if="reveal"
            class="position-absolute w-100"
            height="100%"
            style="bottom: 0;"
        >
          <v-card-text class="pb-0">
            <p class="text-h4">Origin</p>

            <p class="text-medium-emphasis">
              late 16th century (as a noun denoting a place where alms were distributed): from medieval Latin eleemosynarius, from late Latin eleemosyna ‘alms’, from Greek eleēmosunē ‘compassion’
            </p>
          </v-card-text>

          <v-card-actions class="pt-0">
            <v-btn
                color="teal-accent-4"
                text="Close"
                variant="text"
                @click="reveal = false"
            ></v-btn>
          </v-card-actions>
        </v-card>
      </v-expand-transition>
    </v-card>

    <br />

    <v-card
        class="mx-auto"
        max-width="300"
        style="text-align: center"
    >
      <v-card-text>
        <p class="text-h4 font-weight-black">Jack Kallis</p>

        <p>South Africa</p>

        <img src="https://res.cloudinary.com/dyoxubvbg/image/upload/v1577106216/artists/default_m.jpg" />

        <div class="text-medium-emphasis" style="text-align: left">
          <v-row no-gutters>
            <v-col md="6">
              <p>
                <strong>Innings:</strong>
                25
              </p>

              <p>
                <strong>Runs:</strong>
                25786
              </p>

              <p>
                <strong>Balls:</strong>
                25
              </p>

              <p>
                <strong>Average:</strong>
                45.46
              </p>

              <p>
                <strong>Not Outs:</strong>
                72
              </p>

              <p>
                <strong>Highest: </strong>
                172
              </p>

              <p>
                <strong>50/100: </strong>
                25/10
              </p>
            </v-col>

            <v-col md="6">
              <p>
                <strong>Catches</strong>
                123
              </p>

              <p>
                <strong>Wickets:</strong>
                123
              </p>

              <p>
                <strong>Balls: </strong>
                12302
              </p>

              <p>
                <strong>Runs: </strong>
                12302
              </p>

              <p>
                <strong>Fifers: </strong>
                12
              </p>

              <p>
                <strong>Economy: </strong>
                7.85
              </p>

              <p>
                <strong>DOB: </strong>
                24/01/1967
              </p>
            </v-col>
          </v-row>
        </div>
      </v-card-text>
    </v-card>

  </div>

</template>

<script>
export default {
  name: "MyCard",
  data() {
    return {
      reveal: false
    };
  }
}
</script>

<style scoped>

</style>