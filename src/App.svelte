<script>
import Timer from "./Timer.svelte";
import HowTo from "./HowTo.svelte";
</script>

<style> h1,h3 {
	text-align: center;
}
a {
	text-decoration: none;
}
</style>
<h1>Wash your hands!</h1>
<Timer />

<HowTo />

<h3>
	<a href="https://www.who.int/gpsc/clean_hands-protection/en/">Picture Source</a>
	<a href="https://freesound.org/people/metrostock99/sounds/345086/">Sound Source</a>
</h3>

<!-- <button {on:click="dark"}>Dark Mode</button> -->