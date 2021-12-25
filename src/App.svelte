<script lang="ts">
    import Workout from "./Workout.svelte";
</script>

<main>
	<h1>Sessions</h1>
    <ul>
        <li><Workout date="{new Date('2021-12-19')}" /></li>
        <li><Workout date="{new Date()}" /></li>
        <li><Workout date="{new Date('2021-12-21')}" /></li>
    </ul>
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

    ul {
        display: flex;
        width: 100vw;
        overflow-x: scroll;
        scroll-snap-type: x mandatory;
    }

    ul li {
        scroll-snap-align: start;
        width: 100vw;
        padding-left: 2rem;
        padding-right: 2rem;
    }
</style>
