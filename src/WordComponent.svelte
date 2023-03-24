<script>
  export let word;
</script>

<div class="word" on:click>
  <h3 class="word__title">{ word }</h3>
</div>

<style lang="scss">
.word {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 400px;
  height: 100%;
  max-height: 200px;
  border-radius: 20px;
  background-color: rgb(238, 210, 54);
}

.word__title {
    font-size: 20px;
    color: white;
  }
</style>