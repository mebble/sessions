<script lang="ts">
	export let name: string;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
    <div>
        <ul>
            <li>
                <section>
                    <h2>Pull up</h2>
                    <table>
                        <thead>
                            <tr>
                                <th scope="col">Set</th>
                                <th scope="col">Weight</th>
                                <th scope="col">Reps</th>
                                <th scope="col">Done</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <th scope="row">1</th>
                                <td>BW+5 kg</td>
                                <td>999</td>
                                <td>Y</td>
                            </tr>
                            <tr>
                                <th scope="row">2</th>
                                <td>BW+5 kg</td>
                                <td>5</td>
                                <td>N</td>
                            </tr>
                        </tbody>
                    </table>
                    <button>Add set</button>
                </section>
            </li>
        </ul>
    </div>

</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

    /* * {
        border: black solid 1px;
    } */
</style>
