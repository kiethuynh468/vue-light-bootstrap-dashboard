<template>
<div v-if="showDialog" class="return-dialog">
    <div class="return-dialog-content">
    <p class="mess">{{ returnDialogMessage }}</p>
    <button class="btn btn-primary" @click="closeDialog">Close</button>
    </div>
</div>
</template>

<script>
export default {
props: {
    showDialog: Boolean,
    returnDialogMessage: String,
},
methods: {
    closeDialog() {
    this.$emit('close');
    },
},
};
</script>

<style scoped>
/* Add your styling for the dialog here */
.return-dialog {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}

.return-dialog-content {
  background: #fff;
  padding: 20px;
  border-radius: 8px;
  text-align: center; /* Center-align text within the content */
  /* background-color: rgb(238, 235, 235); */
}

.mess {
    padding: 50px 15px;
    /* background-color: rgb(212, 211, 211); */
    /* border-radius: 8px; */
}

.close-button {
  /* Center the button horizontally */
  display: block;
  margin: 0 auto;
  /* Add additional styling as needed */
}
</style>
  