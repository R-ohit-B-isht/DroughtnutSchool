<script>
	export let menuOpen;
</script>

<style>	
/* Dropdown Button */
.dropbtn {
  background-color: darkblue;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}
	
	/* Dropdown button on hover & focus */
.dropbtn:hover, .dropbtn:focus {
  background-color: #3e8e41;
}

</style>
<!-- class="dropbtn" -->
  <button on:click >
    <!-- {!menuOpen ? "Show Menu" : "Close Menu"} -->
    {#if !menuOpen}
         <!-- content here -->
         <h1>Open Menu</h1>
    {:else}
         <!-- else content here -->
         <h1>Close Menu</h1>
    {/if}
</button>
