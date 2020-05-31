<template>
  <div class="d-flex align-center fill-height">
    <v-card class="mx-auto" width="400" outlined>
      <v-card-title>Login</v-card-title>

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

        <v-text-field
          v-model="password"
          @blur="$v.password.$touch()"
          :error-messages="passwordErrors"
          label="Password"
          outlined
          single-line
          dense
          :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
          :type="show ? 'text' : 'password'"
          @click:append="show = !show"
        />

        <v-btn
          primary
          block
          color="accent"
          @click="login"
          :disabled="$v.$invalid"
          >Login</v-btn
        >

        <div class="d-flex flex-row-reverse">
          <router-link
            tag="a"
            class="mt-2 py-2 accent--text"
            style="text-decoration: none"
            to="/forgot"
          >
            <strong>Forgot Password</strong>
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