<!--
@component
Sidebar.svelte — NYCity News Service Style Sidebar Content

A wrapper component that provides a styled sidebar box with
typography that matches the article body.

USAGE EXAMPLE:
<Sidebar>
  <h3>Sidebar title</h3>
  <p>Your sidebar content goes here...</p>
</Sidebar>
-->

<script>
  let {
    children,
  } = $props();
</script>

<aside class="sidebar-box">
  {@render children()}
</aside>

<style lang="scss">
  @use '../styles' as *;

  .sidebar-box {
    font-family: var(--font-sans);
    font-size: var(--font-size-base);
    line-height: 1.75;
    color: var(--color-text);
    background-color: var(--color-light-gray);
    border: var(--border-width-thin) solid var(--color-border);
    border-left: var(--border-width-accent) solid var(--color-accent);
    padding-left: var(--spacing-md);
    margin: var(--spacing-md) 0;
    border-radius: 6px;
    box-shadow: 0 1px 2px var(--color-shadow);
    float: right;
    width: 300px;   
  }

  .sidebar-box :global(p) {
    margin-bottom: var(--spacing-md);
  }

  .sidebar-box :global(p:last-child) {
    margin-bottom: 0;
  }

  .sidebar-box :global(a) {
    color: var(--color-dark);
    text-decoration: underline;
    text-underline-offset: 2px;
  }

  .sidebar-box :global(a:hover) {
    color: var(--color-accent);
  }

  .sidebar-box :global(h2) {
    font-family: var(--font-serif);
    font-size: 1.5rem;
    font-weight: 400;
    margin-top: var(--spacing-sm);
    margin-bottom: var(--spacing-sm);
    color: var(--color-dark);
  }

  .sidebar-box :global(h3) {
    font-family: var(--font-serif);
    font-size: 1.25rem;
    font-weight: 400;
    margin-top: var(--spacing-sm);
    margin-bottom: var(--spacing-sm);
    color: var(--color-dark);
  }

  .sidebar-box :global(blockquote) {
    border-left: var(--border-width-accent) solid var(--color-accent);
    margin: var(--spacing-md) 0;
    padding: var(--spacing-xs) var(--spacing-sm);
    font-style: italic;
    font-size: var(--font-size-lg);
    line-height: 1.6;
    color: var(--color-dark);
    background-color: var(--color-white);
  }

  .sidebar-box :global(blockquote p) {
    margin-bottom: 0;
  }

  .sidebar-box :global(ul),
  .sidebar-box :global(ol) {
    margin-bottom: var(--spacing-md);
    padding-left: var(--spacing-md);
  }

  .sidebar-box :global(li) {
    margin-bottom: var(--spacing-xs);
  }

  .sidebar-box :global(strong) {
    font-weight: 600;
  }

  @include tablet {
    .sidebar-box {
      font-size: var(--font-size-lg);
      line-height: 1.8;
    }

    .sidebar-box :global(blockquote) {
      font-size: var(--font-size-xl);
      padding-left: var(--spacing-md);
    }
  }
</style>

