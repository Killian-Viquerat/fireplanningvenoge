<script>
  export let onExportJson = () => {};
  export let onImportJson = () => {};
  export let onResetConfiguration = () => {};
  let importInput;
</script>

<section class="card">
  <h2>Import / Export JSON</h2>
  <div class="row">
    <button on:click={onExportJson}>Exporter JSON</button>
    <button on:click={() => importInput?.click()}>Importer JSON</button>
    <button class="button-danger" on:click={onResetConfiguration}>Supprimer toute la configuration</button>
    <input bind:this={importInput} type="file" accept="application/json" hidden on:change={onImportJson} />
  </div>
</section>
