<template>
  <v-row>
    <v-col cols="12" lg="4">
      <v-card v-for="(site, index) in sites" :key="index">
        <v-card-title class="subheading font-weight-bold justify-space-between">{{ site.name }} <v-chip color="primary">Active</v-chip></v-card-title>
        <v-divider></v-divider>
        <div>
          <v-card-text>
            <h3>Frameworks:</h3>
            <v-chip>Magento (v2.2)</v-chip>
          </v-card-text>
        </div>
      </v-card>

    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    itemsPerPage: 4,
    sites: [
      {
        name: 'asvineyards.com',
        data: {
          provider: 'GoDaddy',
          ipAddress: '144.16.1.126',
          clientProvided: false,
        },
        libraries: {
          jQuery: '3.3.1',
          Bootstrap: '4.5.1'
        },
        sharedHosting:{
          account: 'vulnerable.shared.com'
        },
        php:{
          version: 5.2
        },
        node:{},
      },
    ],
  }),
}
</script>
