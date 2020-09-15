<template>
  <v-layout
    column
  >
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>
            Project Quick Look
          </v-card-title>
          <v-row>
            <v-col>
              <v-stepper value="3" alt-labels >
                <v-stepper-header>
                  <v-stepper-step step="1" color="green" complete>
                    <div class="text-center">
                      <span class="d-block"><small>Design</small></span>
<!--                      <v-icon>mdi-brush</v-icon>-->
                    </div>
                  </v-stepper-step>
                  <v-divider></v-divider>
                  <v-stepper-step color="green" step="2" complete>
                    <div class="text-center">
                      <span class="d-block"><small>Development</small></span>
<!--                      <v-icon>mdi-code-tags</v-icon>-->
                    </div>
                  </v-stepper-step>
                  <v-divider></v-divider>

                  <v-stepper-step step="3">
                    <div class="text-center" >
                      <span class="d-block"><small>Content</small></span>
<!--                      <v-icon>mdi-content-duplicate</v-icon>-->
                    </div>
                  </v-stepper-step>

                  <v-divider></v-divider>
                  <v-stepper-step step="4" complete-icon="mdi-file-find">
                    <div class="text-center">
                      <span class="d-block"><small>Review</small></span>
<!--                      <v-icon>mdi-file-find</v-icon>-->
                    </div>
                  </v-stepper-step>
                  <v-divider></v-divider>
                  <v-stepper-step step="5" complete-icon="mdi-rocket">
                    <div class="text-center">
                      <span class="d-block"><small>Live</small></span>
<!--                      <v-icon>mdi-rocket</v-icon>-->
                    </div>
                  </v-stepper-step>
                </v-stepper-header>
              </v-stepper>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" lg="3">
        <v-card dark>
          <v-card-title>
            Monthly Budget Summary
          </v-card-title>
          <v-row justify="center">
            <v-col cols="6" class="text-center">
              <v-progress-circular size="150" width="15" color="red" :value="100" >
                <div>
                  <h2>$50.00</h2>
                  Loss
                </div>
              </v-progress-circular>
            </v-col>
            <v-col class="text-left">
              <v-card-text class="pt-0">
                <v-subheader class="pl-0">
                  Income
                </v-subheader>
                <h3 class="green--text">$100</h3>
                <v-subheader class="pl-0">
                  Expenses
                </v-subheader>
                <h3 class="red--text">$150.00</h3>
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" lg="3">
        <v-card dark>
          <v-card-title>
            Monthly Time Summary
          </v-card-title>
          <v-row justify="center">
            <v-col cols="6" class="text-center">
              <v-progress-circular size="150" width="15" color="orange" :value="5/6 * 100" >
                <h2>{{ (5/6 * 100).toFixed(0) }}%</h2>
              </v-progress-circular>
            </v-col>
            <v-col class="text-left">
              <v-card-text class="pt-0">
                <v-subheader class="pl-0">
                  Time Used
                </v-subheader>
                <h3>5 of 6 Hours</h3>
                <v-subheader class="pl-0">
                  Time Remaining
                </v-subheader>
                <h3>1 Hour</h3>
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
export default {}
</script>
