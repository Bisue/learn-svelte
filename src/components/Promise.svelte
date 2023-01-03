<script lang="ts">
  function lazy(delay: number) {
    return new Promise(resolve => {
      setTimeout(() => {
        resolve(delay);
      }, delay);
    });
  }
</script>

{#await lazy(1500)}
  <div>loading...</div>
{:then delay}
  <div>delay: {delay}</div>
  <!-- {:catch error}
  <div>error! - {error.message}</div> -->
{/await}
