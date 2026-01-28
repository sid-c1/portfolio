<script lang="ts">
	import '../app.css';
	import '../pico.sand.min.css';

	let { children } = $props();
</script>
<nav id="nav">
  <div class="brand">
    <a href="#home"><h3>Sridhar Chaturbedi</h3></a>
  </div>
  <div class="links">
    <a href="#projects"><p class="text-xl">Projects</p></a>
    <a href="#skills"><p class="text-xl">Skills & Experience</p></a>
    <a href="#contact"><p class="text-xl">Contact</p></a>
  </div>
</nav>

<div class="content">
  {@render children()}
</div>

<style>
  :global(html) { scroll-behavior: smooth; }

  #nav{
    position:fixed;
    top:0;
    left:0;
    right:0;
    height:5rem;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:1rem;
    padding:0.5rem;
    background:rgb(19,23,31);
    z-index:50;
  }

  #nav .links{ display:flex; gap:1rem; align-items:center; }

  .content{ margin-left:0; margin-top:0; padding:1rem; }

  @media(min-width:768px){
    #nav{
      width:auto;
      height:100%;
      top:0;
      left:0;
      right:initial;
      flex-direction:column;
      align-items:flex-start;
      padding:1.5rem;
      background:transparent;
    }
    #nav .links{ flex-direction:column; gap:0.75rem; }
    .content{ margin-left:12rem; margin-top:0; }
  }

  :global(main section){ width:100%; box-sizing:border-box; }
  :global(img){ max-width:100%; height:auto; display:block; }
</style>
