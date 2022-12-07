<script lang="ts">
    let count: number = 0
    const increment = () => {
        count += 1
    }
</script>

<svelte:options tag="mt-counter" />
<button class="btn btn-success" on:click={increment}>
    カウントアップ: {count}
</button>

