<template>
  <v-app>
    <v-content app>
      <v-container fluid fill-height>
        <v-layout align-center justify-center row>
          <!-- content -->
          <v-flex xs12 sm12 md3>
            <v-card class="elevation-10">
              <!-- logo -->
              <v-layout justify-space-around>
                <v-avatar size="100" class="mt-5 mb-3">
                  <img src="https://avatars1.githubusercontent.com/u/12960236?s=460&v=4" alt="PP">
                </v-avatar>
              </v-layout>
              <!-- end of logo -->
              <v-flex class="px-5 pt-5 pb-5">
                <v-text-field label="Email">
                </v-text-field>
              </v-flex>
              <v-flex class="pb-5 px-5">
                <v-text-field label="Password">
                </v-text-field>
              </v-flex>
              <v-layout class="pb-5 px-5" justify-space-between>
                <v-btn color="primary" class="mx-0">Login</v-btn>
                <v-btn flat small color="primary" class="mx-0 hidden-sm-and-up">Recover password</v-btn>
              </v-layout>
            </v-card>
          </v-flex>
          <!-- end of content -->
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'Login'
}
</script>

