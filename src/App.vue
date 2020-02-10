<template>
  <main>
    <p v-bind:class="{ 'text--alert': !charLeft }">You have {{charLeft}} characters left</p>
    <textarea v-model="value" :maxlength="charMax" placeholder="type your text here"></textarea>
  </main>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      value: '',
      charMax: 100
    }
  },
  computed: {
    charLeft: function () {
      return this.charMax - this.value.length
    }
  }
}
</script>

<style lang="scss">
html,body{
  height: 100%;
  background: #EDF2F7;
}
body{
  font-family: sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #3B4958;
}
main{
  text-align: center;
}
textarea{
  width: 300px;
  height: 200px;
  padding: 10px;
  border-radius: 3px;
  resize: none;
  border: none;
  box-shadow:
    0 4.5px 3.6px rgba(0, 0, 0, 0.024),
    0 12.5px 10px rgba(0, 0, 0, 0.035),
    0 30.1px 24.1px rgba(0, 0, 0, 0.046),
    0 100px 80px rgba(0, 0, 0, 0.07)
  ;

}
.text--alert{
  color: #ff0000
}
</style>
