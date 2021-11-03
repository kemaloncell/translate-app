<template>
  <div class="container">
    <h1 class="text-center">Vue-Translator</h1>
    <h5 class="text-center">Vue.js ile Translator</h5>
    <br />
    <div class="row">
      <div class="col-md-12 text-center">
        <TranslateForm @translatedEvent="translatedText = $event" @historyEvent="history.push($event)" />
        <h3 class="text-success text-center">{{ translatedText }}</h3>
        <SearchHistory :history="history" />
      </div>
    </div>
  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm.vue';
import SearchHistory from './components/SearchHistory.vue';
export default {
  components: {
    TranslateForm,
    SearchHistory,
  },
  data() {
    return {
      translatedText: '',
      history: [],
    };
  },
};
</script>

<style scoped>
body {
  background-color: #dedede;
}
</style>
