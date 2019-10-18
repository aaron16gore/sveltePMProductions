<script>
	import Greeting from './Greeting.svelte'
	import Login from "./Login.svelte";
	import FramewworkList from "./FrameworkList.svelte";
	import FrameworkList from "./FrameworkList.svelte";
	import EventDemo from './EventDemo.svelte';
	import BindingDemo from './BindingDemo.svelte'
	
	export let name;

	let numbers = [1, 2, 3, 4];

	function addNumber() {
		numbers = [...numbers, numbers.length + 1];
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>


