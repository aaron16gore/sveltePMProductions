<script>
    export let first_name;
    export let last_name;
    
    $: name = first_name + " " + last_name;
</script>

<style>
    h2 {
        color: yellow;
        font-family: 'Comic Sans MS';
        font-size: 2em;
    }
</style>

<h2>Hello there {name}!</h2>