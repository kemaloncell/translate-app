<template>
  <div class="well" v-if="history.length > 0">
    <h3>Search History</h3>
    <ul class="list-group text-left">
      <li class="list-group-item" v-for="(items, i) in history" :key="i">
        <div>
          <strong>{{ items.from }} => {{ items.to }}</strong>
        </div>
        <br />
        <div>
          <strong class="text-success">{{ items.translateText }} : </strong>
          <span class="text-info">{{ items.translatedText }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['history'],
};
</script>

<style scoped></style>
