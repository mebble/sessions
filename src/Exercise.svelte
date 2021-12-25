<script lang="ts">
    import type { ExerciseSet } from './types';

    export let name: string;

    let sets: ExerciseSet[] = [
        { weight: 'BW+5', reps: 999, done: true },
        { weight: 'BW+5', reps: 5, done: false },
    ];

    function addSet() {
        const lastSet = sets[sets.length - 1];
        console.log(lastSet)
        sets = [
            ...sets,
            { weight: lastSet.weight, reps: lastSet.reps, done: false }
        ]
    }
</script>

<section>
    <h2>{name}</h2>
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
            {#each sets as set, i}
                <tr>
                    <th scope="row">{i+1}</th>
                    <td><input type="text" name="set-{i+1}-weight" bind:value="{set.weight}">kg</td>
                    <td><input type="number" name="set-{i+1}-reps" bind:value="{set.reps}"></td>
                    <td><input type="checkbox" name="set-{i+1}-done" bind:checked="{set.done}"></td>
                </tr>
            {/each}
        </tbody>
    </table>
    <button on:click={addSet}>Add set</button>
</section>

<style>
    section {
        display: flex;
        flex-direction: column;
    }

    h2 {
        text-align: left;
    }

    input {
        width: 5ch;
    }
</style>
