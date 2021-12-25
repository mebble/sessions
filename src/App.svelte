<script lang="ts">
    import Workout from "./Workout.svelte";
</script>

<main>
	<h1>Sessions</h1>
    <Workout />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
</style>
