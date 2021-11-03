<template>
  <form @submit.prevent="translateIt" class="well">
    <textarea v-model="translateText" cols="30" rows="5" class="form-control" placeholder="Write the word/sentence you want to translate."></textarea>
    <select v-model="translateTo" class="form-control">
      <option>1</option>
    </select>
    <br />
    <div class="text-left">
      <strong>Detected Language : </strong>
    </div>
    <br />
    <button type="submit" class="btn btn-primary btn-block">Translate!</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      translateText: '',
      translateTo: '',
    };
  },
  methods: {
    translateIt() {
      alert(this.translateText);
      alert(this.translateTo);
    },
  },
};
</script>

<style scoped></style>
