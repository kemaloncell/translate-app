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
import axios from 'axios';
export default {
  data() {
    return {
      translateText: '',
      translateTo: '',
    };
  },
  methods: {
    translateIt() {
      let url = ' https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20211103T140348Z.9b8263362c116e09.c63c447acbe03118235c2c0fdf3566420e0cd318&text=' + this.translateText + '&lang=en';

      axios
        .get(url)
        .then((response) => {
          console.log(response);
        })
        .catch((e) => console.log(e));
    },
  },
};
</script>

<style scoped></style>
