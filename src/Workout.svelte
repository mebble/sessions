<script lang="ts">
    import type { Exercise as ExerciseType } from './types';
    import Exercise from './Exercise.svelte';

    export let date: Date;

    let exercises: ExerciseType[] = [
        { name: 'Pull up' },
        { name: 'Squat' }
    ];
</script>

<section>
    <h2>{date.toLocaleDateString()}</h2>
    <ul>
        {#each exercises as exercise}
            <li>
                <Exercise name="{exercise.name}" />
            </li>
        {/each}
    </ul>
</section>
