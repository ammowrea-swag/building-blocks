<!--

@component
AuthorBox.svelte — NYCity News Service Style Author Box

A wrapper component that provides a styled author box with
typography that matches the article body.

USAGE EXAMPLE:
<AuthorBox>
  <h3>Author name</h3>
  <p>Author bio goes here...</p>
</AuthorBox>
-->

<script>
  export let name = "Author Name";
  export let avatarUrl = "https://via.placeholder.com";
  export let bio = "Short author description.";
</script>

<div class="author-box">
  <img src={avatarUrl} alt={name} class="avatar" />
  <div class="info">
    <h3>About {name}</h3>
    <p>{bio}</p>
  </div>
</div>

<style> 
 .author-box {
    margin-top: var(--spacing-xl);
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

   .avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
  }

    /* Responsive layout for smaller screens */
  @media (max-width: 600px) {
    .author-box {
      flex-direction: column;
      text-align: center;
    }
  }
</style>

