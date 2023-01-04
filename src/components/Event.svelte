<script>
  let m = { x: 0, y: 0 };
  
  function handleMousemove(event) {
    m.x = event.clientX;
	m.y = event.clientY;
  }
</script>

<div on:mousemove={handleMousemove}>
	The mouse position is {m.x} x {m.y}
</div>

<style>
  div {
    width: 250px;
    height: 250px;
    border: 1px solid lightgray;
  }
</style>
