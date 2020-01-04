<div class="container">
  {#if snack}
    <Snack on:eatsnack={() => { snack = false }} />
  {:else}
    <span class="grayed">No snacks for you.</span>
  {/if}
</div>

<script>
  import Snack from './Snack.svelte';

  let snack = true;
</script>
