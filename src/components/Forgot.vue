<template>
  <div class="d-flex align-center fill-height">
    <v-card class="mx-auto" width="400" outlined>
      <v-card-title>Forgot Password</v-card-title>

      <v-card-text>
        <v-text-field
          v-model="email"
          @blur="$v.email.$touch()"
          :error-messages="emailErrors"
          label="Email"
          outlined
          single-line
          dense
          clearable
        />

        <v-btn
          primary
          block
          color="accent"
          @click="reset"
          :disabled="$v.$invalid"
          >Reset</v-btn
        >

        <div class="d-flex">
          <router-link
            tag="a"
            class="mt-2 py-2 accent--text"
            style="text-decoration: none"
            to="/login"
          >
            <strong>Back to Login</strong>
          </router-link>
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
        
}
</script>