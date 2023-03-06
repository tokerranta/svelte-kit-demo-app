<script>
  export let onClick;
</script>

<button {onClick}>
  Hello
</button>

<style>
  button {
    background: var(--color-primary, red);
    transition: background .5s ease;
    border: none;
    padding: .5em 1em;
    text-transform: uppercase;
  }
  
  button:hover {
    background: var(--color-secondary, red);
    cursor: pointer;
  }
</style>