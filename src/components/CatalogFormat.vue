<template>
<form>
  <div class="catTitle" @click="toggleDetails">
      <h3>{{ catHeader }}</h3>
  </div>
  <div class="catDetails" v-if="details">
          <textarea v-model="catBody"></textarea>
  </div>
</form>
</template>

<script>
export default {
    data() {
        return {
            catHeader: 'Test',
            catBody: 'Lets see if this works',
            details: false
        }
    },
    methods: {
        toggleDetails() {
            this.details = !this.details
        }
    }

}
</script>

<style>
    form {
        max-width: 680px;
        width: 100%;
        display: inline-block;
        border: none;
        border-radius: 6px;
        background: whitesmoke;
        padding: 10px;
        text-transform: uppercase;
        text-align: left;
        border-left: solid rgb(255, 103, 2);
    }
    textarea {
        border: none;
        width: 100%;
        height: 100px;
    }
    .catTitle {
        color: black;
    }
    .catDetails {
        border-bottom: solid rgb(255, 103, 2);
    }
</style>