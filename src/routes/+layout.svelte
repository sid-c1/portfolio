<script lang="ts">
    import '../app.css';
    import '../pico.sand.min.css';
    import cv from '$lib/Sridhar Chaturbedi CV.pdf'

    let { children } = $props();

    let showMenu = $state(false);
    const toggleMenu = () => (showMenu = !showMenu);
    const closeMenu = () => (showMenu = false);
</script>

<nav id="nav" class="fixed top-0 left-0 right-0 z-50 bg-[#13171f] flex items-center justify-between p-3 md:bg-transparent md:p-0">
  <div class="brand bg-[rgb(19,23,31)]">
    <a href="/"><h3>Sridhar Chaturbedi</h3></a>
  </div>

  <!-- Mobile menu button (visible only on mobile <768px) -->
  <button
    class="mobile-menu md:hidden absolute right-3 top-3 w-12 h-12 flex items-center justify-center bg-transparent border-0 z-60"
    aria-label="Toggle menu"
    aria-expanded={showMenu}
    onclick={toggleMenu}
    class:open={showMenu}
  >
    <span></span>
    <span></span>
    <span></span>
  </button>

  <div class="links hidden md:flex md:flex-col md:gap-3 md:items-start md:fixed md:left-4 md:bottom-4">
    <a href={cv} download class="text-xl">CV</a>
    <a href="#projects" class="text-xl">Projects</a>
    <a href="#skills" class="text-xl">Skills & <br>Experience</a>
    <a href="#contact" class="text-xl">Contact</a>
  </div>
</nav>

<!-- Mobile modal overlay -->
<div
  class="fixed inset-0 bg-black/60 flex items-center justify-center transition-opacity z-50 {showMenu ? 'opacity-100 pointer-events-auto' : 'opacity-0 pointer-events-none'}"
  onclick={closeMenu}
  aria-hidden={!showMenu}
>
  <div
    class="bg-[#0f1317] p-8 rounded-lg w-11/12 max-w-sm"
    role="dialog"
    tabindex="-1"
    onclick={(e) => e.stopPropagation()}
    onkeydown={(e) => e.key === 'Escape' && closeMenu()}
  >
    <nav class="flex-col">
      <a href="#home" class="block py-3 text-white text-lg" onclick={closeMenu}>Home <br></a>
      <a href="#projects" class="block py-3 text-white text-lg" onclick={closeMenu}>Projects</a>
      <a href="#skills" class="block py-3 text-white text-lg" onclick={closeMenu}>Skills & Experience</a>
      <a href="#contact" class="block py-3 text-white text-lg" onclick={closeMenu}>Contact</a>
      <a href={cv} download class="block py-3 text-white text-lg" onclick={closeMenu}>CV</a>
    </nav>
  </div>
</div>

<div class="content mt-0 p-4">
  {@render children()}
</div>

<style>
  :global(html) { scroll-behavior: smooth; }

  /* minimal custom CSS kept for hamburger transform */
  .mobile-menu span{
    display:block;
    width:22px;
    height:2px;
    background:#fff;
    margin:4px 0;
    transition: transform .25s ease, opacity .2s ease;
  }
  .mobile-menu.open span:nth-child(1){ transform: translateY(6px) rotate(45deg); }
  .mobile-menu.open span:nth-child(2){ opacity:0; }
  .mobile-menu.open span:nth-child(3){ transform: translateY(-6px) rotate(-45deg); }

  :global(main section){ width:100%; box-sizing:border-box; }
  :global(img){ max-width:100%; height:auto; display:block; }
  :global(main section){ width:100%; box-sizing:border-box; }
  :global(img){ max-width:100%; height:auto; display:block; }
</style>
