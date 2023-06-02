<script>
    export let person = 'valueInChild'
    import { createEventDispatcher } from 'svelte';
    import { get_current_component } from 'svelte/internal';
    const component = get_current_component();
    const originalDispatch = createEventDispatcher();

    const dispatch = (person, detail) => {
       originalDispatch(person, detail);
       component?.dispatchEvent(new CustomEvent(person, { detail }));
    }

    $: (person) && dispatch('personChange', { person })
</script>
<svelte:options tag="text-input" />
<textarea bind:value={person}></textarea>

<style>
  textarea { width: 100%; height: 200px; }
</style>

