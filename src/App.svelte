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
        width: 85vw;
        max-width: 500px;
        margin: auto;
        overflow-x: scroll;
        /* https://css-tricks.com/practical-css-scroll-snapping/#example-2-horizontal-slider */
        scroll-snap-type: x mandatory;
    }

    ul li {
        scroll-snap-align: start;
        /* https://stackoverflow.com/a/30684798 */
        flex-shrink: 0;
        width: 100%;
    }
</style>
