<template>
  <div id="app">
    <h2>Stimuchat</h2>
    <section>
      <ChatForm/>
       <ShowChat/>
    </section>
  </div>
</template>

<script>
import ChatForm from './components/form-chat.vue'
import ShowChat from './components/show-chat.vue'

export default {
  name: 'App',
  components: {
    ChatForm,
    ShowChat
  }
}
</script>

<style>
#app {
  width: 40%;
  margin: 0 auto;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
}
section {
  display: flex;
  justify-content: space-between;
}
h2 {
  text-align: center;
}
</style>
