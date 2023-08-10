<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            label="Prepend"
            prepend-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            label="Prepend inner"
            prepend-inner-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            label="Append"
            append-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            label="Append outer"
            append-outer-icon="mdi-map-marker"
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            solo
            label="Prepend"
            prepend-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            solo
            label="Prepend inner"
            prepend-inner-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            solo
            label="Append"
            append-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            solo
            label="Append outer"
            append-outer-icon="mdi-map-marker"
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            filled
            label="Prepend"
            prepend-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            filled
            label="Prepend inner"
            prepend-inner-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            filled
            label="Append"
            append-icon="mdi-map-marker"
          ></v-text-field>

          <v-text-field
            filled
            label="Append outer"
            append-outer-icon="mdi-map-marker"
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            outlined
            label="Prepend"
            prepend-icon="mdi-map-marker"
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      firstname: '',
      lastname: '',
      nameRules: [
        value => {
          if (value) return true

          return 'Name is required.'
        },
        value => {
          if (value?.length <= 10) return true

          return 'Name must be less than 10 characters.'
        },
      ],
      email: '',
      emailRules: [
        value => {
          if (value) return true

          return 'E-mail is requred.'
        },
        value => {
          if (/.+@.+\..+/.test(value)) return true

          return 'E-mail must be valid.'
        },
      ],
    }),
  }
</script>
