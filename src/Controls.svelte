<script lang="ts">
    export let data;

    const increaseValue = () => {
        data.ruleNumber = data.ruleNumber+1;
    }
</script>

<main>
    <div>
        <span>data : {JSON.stringify(data)}</span>
        <button on:click={increaseValue}>Increase Value</button>
    </div>
</main>
