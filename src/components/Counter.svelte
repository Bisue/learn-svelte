<script lang="ts">
let count = 0;

function increase() {
    count++;
}

function decrease() {
    count--;
}
</script>

<div>
    <span>{count}</span>
    <button on:click={increase}>Up</button>
    <button on:click={decrease}>Down</button>
</div>
