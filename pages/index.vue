<template>
  <v-layout
    column
  >
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>
            Project Overview
          </v-card-title>
          <v-card-text>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" lg="4">
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
      <v-col cols="12" lg="4">
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
      <v-col cols="12">
        <v-expansion-panels>
          <v-expansion-panel>
            <v-expansion-panel-header class="headline">
              Overview
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <div>Start Date:</div>
              <div>Estimated Launch Date:</div>
              <div>Launch Date:</div>
              <div>Project Status: Active</div>
              <div>Cancellation Date:</div>
            </v-expansion-panel-content>
          </v-expansion-panel>
          <v-expansion-panel>
            <v-expansion-panel-header class="headline">
              Domains & DNS
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <div>Domain Name: example.com</div>
              <div>Subdomains: None</div>
              <div>Name Servers: Cloudflare</div>
              <div>Name Server Cost: Free</div>
              <div>Domain Cost: $9.99 Yearly</div>
            </v-expansion-panel-content>
          </v-expansion-panel>
          <v-expansion-panel>
            <v-expansion-panel-header class="headline">
              Hosting
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <div>Hosted In House: True</div>
              <div>Hosting Provider: GoDaddy</div>
              <div>Hosting Type: Shared Hosting</div>
              <div>Shared Hosting Account: shared.vulnerablehost.com</div>
              <div>Hosting Cost: $9.99 Monthly</div>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
export default {
}
</script>
