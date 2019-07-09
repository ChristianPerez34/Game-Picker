<script>
  import { onMount } from "svelte";
  import axios from "axios";
  // export the variable to make a prop
  export let url = "https://jsonplaceholder.typicode.com/todos";
  let data = [];
  onMount(async function() {
    axios.get(url).then(response => {
      data = response.data;
    });
  });
</script>

<!-- {@debug data} -->
<ul>
  {#each data as link}
    <li>
      <a href={link.url}>{link.title}</a>
    </li>
  {/each}
</ul>
