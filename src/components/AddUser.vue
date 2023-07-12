<template>
  <div>
    <v-btn 
      color="primary" 
      dark
      @click="openDialog"
    >
      Open Dialog
    </v-btn>

    <v-dialog v-model="dialogVisible" max-width="500px">
      <v-card>
        <v-card-title>
          <span class="headline">Dialog Title</span>
        </v-card-title>
        <v-card-text>
          <!-- Dialog content goes here -->
          This is the content of the dialog.
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" @click="save">Save</v-btn>
          <v-btn color="secondary" @click="cancel">Cancel</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false
    };
  },
  methods: {
    openDialog() {
      this.dialogVisible = true; // Open the dialog
      console.log("Open dialog is clicked", this.dialogVisible)
    },
    save() {
      this.dialogVisible = false; // Close the dialog
    },
    cancel() {
      this.dialogVisible = false; // Close the dialog
    }
  }
};
</script>