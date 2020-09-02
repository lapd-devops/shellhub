<template>
  <fragment>
    <v-snackbar
      v-model="snackbar"
      :timeout="4000"
    >
      Device SSHID copied to clipboard.
    </v-snackbar>
  </fragment>
</template>

<script>

export default {
  name: 'SnackbarCopy',

  computed: {
    snackbar: {
      get() {
        return this.$store.getters['modals/snackbarCopy'];
      },

      set() {
        this.$store.dispatch('modals/unsetShowStatusSnackbarCopy');
      },
    },
  },
};

</script>
