<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      clipped-left
      fixed
      app
    >
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
      />
      <div class="mt-7 ml-5"  @click.stop="projectDrawer = !projectDrawer">
        <v-select dense
                  label="Current Project"
                  :items="projects"
                  :menu-props="{ bottom: true, offsetY: true }"
                  outlined
                  @click.stop="projectDrawer = !projectDrawer"
                  :value="selectedProject"
        />
      <v-spacer />
      </div>


    </v-app-bar>
    <v-main>
      <v-container>
        <template>
          <transition name="fade-transition">
            <nuxt />
          </transition>
        </template>
      </v-container>
    </v-main>
    <v-footer
      app
    >
      <span>&copy; Josh Mielke </span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      projectDrawer: false,
      selectedProject: null,
      projects: ['Abstract Sensualism Vineyards', 'Blauers', 'Robertson\'s Honda'],
      items: [
        {
          icon: 'mdi-apps',
          title: 'Summary',
          to: '/'
        },
        {
          icon: 'mdi-server',
          title: 'Hosting',
          to: '/hosting'
        },
        {
          icon: 'mdi-laptop',
          title: 'Website',
          to: '/website'
        },
      ],
      title: 'Project Details'
    }
  },
  created(){
    this.selectedProject = this.projects[0];
  }
}
</script>
