<script lang="ts">
  import { createEventDispatcher } from 'svelte'
  const dispatch = createEventDispatcher()
  const message = 'Child Value'

  function sayHello() {
    dispatch('sayHello', { message })
  }
  export let title
</script>

<svelte:options tag="text-props" />

<div>
  <button on:click={sayHello}>clickMe</button>
  Props: {title}
</div>
