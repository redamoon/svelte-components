<script>
    import { marked } from 'marked';
    let value = `Movable Type`;
</script>

<svelte:options tag="my-text" />

<textarea bind:value={value}></textarea>
<p>本文の入力</p>
<div>{@html marked(value)}</div>

<style>
  textarea { width: 100%; height: 200px; }
</style>
