<template>
  <div class="message">
    <p>Discussion créée par <strong>{ item.name }</strong></p>
    <p>(Sur le thème : <strong>{ item.theme }</strong> )</p>
    <p>Dans le groupe <span>{ item.theme }</span></p> 
    <q>{ item.message }</q>
  </div>
</template>

<script>
  export default {
    props: {
      item: {
        required: true
      },
    },
  }
</script>