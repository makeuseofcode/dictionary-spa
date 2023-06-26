<script>
  import { navigate } from "svelte-routing";
  let enteredWord;
</script>

<main class="homepage">
  <div class="dictionary-text">Dictionary</div>
  <form on:submit|preventDefault={() => navigate(`/find/${enteredWord.toLowerCase()}`)}>
    <input
      type="text"
      bind:value={enteredWord}
      placeholder="Begin your search..."
      autofocus
    />
    {#if enteredWord}
      <button type="submit">Search Word</button>
    {/if}
  </form>
</main>
