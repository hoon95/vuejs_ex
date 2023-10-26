<script>
export default {
  data() {
    return {
      list: [
        'html','css', 'javascript'
      ]
    }
  },
  mounted() {
    this.$refs.username.focus()
    console.log(this.$refs.items)
    // document.querySelector('#username').focus();
  }
}
</script>

<template> 
  <div class="layout">
    <h1>This is refs page</h1>
    <input ref="username" />
    <!-- <input type="text" id="username"> -->
    <hr>
    <ul>
    <li v-for="item in list" ref="items" :key="item.id">
      {{ item }}
    </li>
  </ul>
  </div>
</template>

<style>

</style>