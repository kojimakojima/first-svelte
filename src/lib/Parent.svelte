<script lang="ts">
  import Child from "./Child.svelte";

  let greeting = "Let's play with Svelte!";
  let num = 2024;
</script>

<Child message={greeting} {num} />
