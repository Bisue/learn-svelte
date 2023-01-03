<script>
  let lists = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
</script>

<!-- <ul>
  {#each lists as list}
    <li>{list}</li>
  {/each}
</ul> -->

<!-- <ul>
  {#each lists as list, idx}
    <li>{list}</li>
  {/each}
</ul> -->

<ul>
  {#each lists as list (list)}
    <li>{list}</li>
  {/each}
</ul>
