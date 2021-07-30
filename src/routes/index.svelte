<script context="module">
  import { writable } from "svelte/store";

  export async function load({ page }) {
    const { query } = page;
    const name = query.get('name');
    console.log("load", name)
    return { props: { name } };
  }
</script>
  <script>
    export let name;
  </script>
<h1>Welcome to SvelteKit</h1>
{name}
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
