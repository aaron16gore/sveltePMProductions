<script>
    let lastY = 0;
    let headerClass='pin';
    function changeClass(y) {
        let result = headerClass;
        const scrolledPxs = lastY - y;
        const scrollDirection = scrolledPxs < 0 ? "down" : "up"
        lastY = y;
        return result;
    }   
    $: headerClass = changeClass(y);
    
</script>

<style>
    header {
        background-color: darkgrey;
        height: 80px;
        width: 150%;
        margin: 0;
        padding: 0;
        transition: all 0.3s linear;
    }
    .pin {
        top: 0;
    }
    .unpin {
        top: -80px;
    }
    
    main {
        min-height: 150vh;
        padding-top: 80px;
    }
</style>

<svelte:window bind:scrollY={y}/>
<header class={headerClass}></header>
<main>Lorem ipsum</main>