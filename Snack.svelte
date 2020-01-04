<script>
  import { onMount } from 'svelte'
  import Snackbar, {Actions, Label} from '@smui/snackbar';
  import Button from '@smui/button';
	import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();

  let snackbar

  onMount(() => {
    snackbar.open()
  })

  function eatSnack () {
    dispatch('eatsnack')
  }
</script>

<Snackbar leading timeoutMs={10000} bind:this={snackbar}>
  <Label>Tasty snack.</Label>
  <Actions>
    <Button on:click={eatSnack}>Eat it</Button>
  </Actions>
</Snackbar>
