<script lang="ts">
  let count = 0;
  $: multiplied = count * 10;
  $: console.log('actions count:', count);
  $: {
    console.log('=========================');
    console.log('action block count:', count);
    console.log('=========================');
  }
  $: if (count >= 10) {
    console.log('=========================');
    console.log('action block count(>= 10):', count);
    console.log('=========================');
  }

  function increase() {
    count++;
  }

  function decrease() {
    count--;
  }
</script>

<div>
  <span class="count">{count}({multiplied})</span>
  <button on:click={increase}>Up</button>
  <button on:click={decrease}>Down</button>
</div>

{#if count > 10}
  <div>A</div>
{:else if count > 5}
  <div>B</div>
{:else}
  <div>C</div>
{/if}

<style>
  .count {
    font-weight: bold;
  }

  button {
    background: none;
    outline: none;
    border: none;
    border-radius: 3px;
    border: 1px solid #afafaf;
    background: #ededed;
    padding: 0.5rem 1rem;
    cursor: pointer;
    transition: all 0.25s;
  }

  button:hover {
    background: rgb(219, 219, 219);
  }
</style>
