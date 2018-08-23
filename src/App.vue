<template>
  <v-app>
    <v-navigation-drawer 
      app
      clipped
      fixed
      :value=drawer
    >
      <v-list>
        <v-list-tile 
          v-for="data in drawerData"
          :key="data.icon"
        >
          <v-list-tile-action>
            <v-icon>{{ data.icon }}</v-icon>
          </v-list-tile-action>
          
          <v-tile-content>
            <v-tile-title>{{ data.title }}</v-tile-title>
          </v-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    
    <v-toolbar 
      app
      clipped-left
      fixed
    >
      <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-spacer></v-spacer>
      <v-menu 
        offset-y 
        left
        :nudge-bottom=10
      >
        <v-btn 
          icon 
          slot="activator"
        >
          <v-avatar 
            size="40"
          >
            <img src="https://avatars1.githubusercontent.com/u/12960236?s=460&v=4" alt="" srcset="">
          </v-avatar>
        </v-btn>

        <!-- Card -->
        <v-card>
          <v-list>
            <v-list-tile avatar>
              <v-list-tile-avatar>
                <img src="https://avatars1.githubusercontent.com/u/12960236?s=460&v=4" alt="" srcset="">
              </v-list-tile-avatar>

              <v-list-tile-content>
                <v-list-tile-title>One Punch Man</v-list-tile-title>
                <v-list-tile-sub-title>saitama@gmail.com</v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>

          <v-divider></v-divider>
          
          <v-card-actions>
            <v-layout justify-space-around>
              <v-btn flat @click="menu = false">Profile</v-btn>
              <v-btn color="primary" flat @click="menu = false">Logout</v-btn>
            </v-layout>
          </v-card-actions>
          
        </v-card>

      </v-menu>
    </v-toolbar>

    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>

    <v-footer app></v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      items: [
        { title: 'deez'},
        { title: 'nuts'}
      ],
      message: false,
      hints: false,
      fav:false,
      drawer: false,
      drawerData: [
        { icon: 'dashboard', title: 'Dashboard' },
        { icon: 'supervisor_account', title: 'Users' }
      ],
      users: {
        admins: {
          count: 10
        },
        endUsers: {
          count: 115
        }
      }
    }
  }
};
</script>