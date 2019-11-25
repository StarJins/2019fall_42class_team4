<template>
  <v-container fluid grid-list-md>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card>
          <v-card-title primary-title>
            <h3 class="headline mb-0">Mypage</h3>
          </v-card-title>
          <v-card-text>
            <v-text-field
              v-model="email"
              label="e-mail"
              solo
              disabled
           ></v-text-field>
            <v-text-field
              v-model="password"
                :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
                :type="show ? 'text' : 'password'"
              label="password"
              @click:append="show = !show"
              solo
            ></v-text-field>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" @click="modify">수정</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      email: 'test@abc.xyz',
      password: '',
      show: false
    }
  },
  methods: {
    modify: () => {
      console.log('수정')
    }
  }
}
</script>
