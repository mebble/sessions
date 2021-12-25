<script lang="ts">
    import type { Exercise as ExerciseType } from './types';
    import Exercise from './Exercise.svelte';

    let exercises: ExerciseType[] = [
        { name: 'Pull up' },
        { name: 'Squat' }
    ];
</script>

<section>
    <ul>
        {#each exercises as exercise}
            <li>
                <Exercise name="{exercise.name}" />
            </li>
        {/each}
    </ul>
</section>

<style>
    ul {
        padding: 0;
        list-style: none;
    }
</style>
