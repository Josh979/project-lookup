<template>
  <div>
    <v-data-iterator
        :items="items"
        :items-per-page.sync="itemsPerPage"
        hide-default-footer
      >
        <template v-slot:default="props">
          <v-row>
            <v-col
              v-for="item in props.items"
              :key="item.name"
              cols="12"
              sm="6"
              md="4"
              lg="3"
            >
              <v-card>
                <v-card-title class="subheading font-weight-bold justify-space-between">{{ item.name }} <v-chip color="primary">Active</v-chip></v-card-title>

                <v-divider></v-divider>

                <v-list dense>
                  <v-list-item v-for="(value, key) in item.data" :key="key">
                    <v-list-item-content>{{ key }}:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ value }}</v-list-item-content>
                  </v-list-item>
                </v-list>

                <div v-if="item.sharedHosting">
                  <v-divider></v-divider>
                  <v-subheader>Shared Hosting</v-subheader>
                  <v-list class="pt-0" dense>
                    <v-list-item v-for="(value, key) in item.sharedHosting" :key="key">
                      <v-list-item-content>{{ key }}:</v-list-item-content>
                      <v-list-item-content class="align-end">{{ value }}</v-list-item-content>
                    </v-list-item>
                  </v-list>
                </div>

                <div v-if="item.sharedHosting">
                  <v-divider></v-divider>
                  <v-subheader>Libraries</v-subheader>
                  <v-list class="pt-0" dense>
                    <v-list-item v-for="(value, key) in item.libraries" :key="key">
                      <v-list-item-content>{{ key }}:</v-list-item-content>
                      <v-list-item-content class="align-end">{{ value }}</v-list-item-content>
                    </v-list-item>
                  </v-list>
                </div>

              </v-card>
            </v-col>
          </v-row>
        </template>
    </v-data-iterator>
  </div>
</template>

<script>
export default {
  data: () => ({
    itemsPerPage: 4,
    items: [
      {
        name: 'Shared Hosting',
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
