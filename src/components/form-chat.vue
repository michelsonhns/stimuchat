<template>
  <form @submit.prevent="create">
    <div class="form-group">
      <input placeholder="Nom d'utilisateur" type="text" id="author" v-model="author"/>
    </div>
    <div class="form-group">
      <select name="type" id="">
        <option value="">theme</option>
      </select>
    </div>
    <div class="form-group">
      <label for="public">public
        <input type="radio" id="public" value="public" name="accessibility" v-model="accessibility"/>
      </label>
      <label for="privite">prive
        <input type="radio" id="privite" value="privite" name="accessibility"  v-model="accessibility"/>
      </label>
    </div>
    <div class="form-group">
      <textarea class="Message" type="text" id="text" cols="30" rows="10" v-model="text"></textarea>
    </div>
    <button type="submit">Create</button>
  </form>
</template>

<script>
  export default {
    data() {
      return {
        author: "",
        privaticy: "",
        text: "",
      }
    },
    methods: {
      create() {
        const chat = {
          author: this.author,
          privaticy: this.privaticy,
          text: this.text
        };
        this.author = "";
        this.privaticy = "";
        this.text = "";
      }
    },
  }
</script>

<style scoped>
div {
  margin-bottom: 1em;
}
</style>