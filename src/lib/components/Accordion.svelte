<script>
  export let mainHeader = '';
  export let items = [];

  let openIndex = null;

  function toggle(index) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<style>
  .accordion {
    padding-top: 20px;
    width: 100%;
    border-radius: 5px;
    margin-bottom: 10px;
  }
  .accordion-header {
    font-size: 1.25rem;
    padding: 10px;
    cursor: pointer;
    background-color: #f1f1f1;
    border-bottom: 1px solid #ccc;
    width: 100%;
    text-align: left;
    border: none;
  }
  .accordion-content {
    padding: 10px;
    display: none;
  }
  .accordion-content.open {
    display: block;
  }

  .main-header {
   display: flex;
    align-items: center;
    gap: var(--spacing-sm);
    font-family: var(--font-sans);
    font-size: var(--font-size-sm);
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--color-dark);
    margin-bottom: var(--spacing-md);

    &::after {
      content: '';
      flex: 1;
      height: 2px;
      background-color: var(--color-accent);
    }
}
</style>

<div class="accordion">
  {#if mainHeader}
    <div class="main-header">{mainHeader}</div>
  {/if}
  {#each items as item, index}
    <button
      class="accordion-header"
      type="button"
      on:click={() => toggle(index)}
      aria-expanded={openIndex === index}
    >
      {item.header}
    </button>
    <div class="accordion-content {openIndex === index ? 'open' : ''}">
      <p>{item.content}</p>
    </div>
  {/each}
</div>
