<script lang="ts">
import Controls from './components/Controls.svelte';
import Simulation from './components/Simulation.svelte';

const appData = {
    ruleNumber: 46
}
</script>

<main>
    <h1>Circular automata</h1>
    <Controls data={appData} />
    <Simulation data={appData} />
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
</style>
