<script>
    let m = {x: 0, y: 0};
    
    function handleMousemove(event) {
        m.x = event.clientX;
        m.y = event.clientY;
    }
</script>

<style>
    div {
        width: 300px;
        height: 300px;
        color: purple;
        background: lightseagreen;
    }
</style>

<div on:mousemove={handleMousemove}>
    The mouse position is {m.x} x {m.y}
</div>