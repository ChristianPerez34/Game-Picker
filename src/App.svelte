<script>
  import Fetch from "./Fetch.svelte";
  export let name;
</script>

<style>
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
  }

  li {
    float: left;
  }

  li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }

  li a:hover:not(.active) {
    background-color: #777;
  }

  .active {
    background-color: #BBB;
  }
</style>

<ul>
  <li><a class="active" href="#home">Home</a></li>
  <li><a href="#login">Login</a></li>
  <li><a href="#signup">Sign-Up</a></li>
</ul>

<Fetch />
