<script lang="ts">
	import '../app.css';
	import '../pico.sand.min.css';

	let { children } = $props();
</script>
<div class="p-10 flex-col max-w-fit">
  <a href="/">
    <h3>Sridhar Chaturbedi</h3>
  </a>
  <a href="/skills">
    <p class="text-xl">Skills & Experience</p>
  </a>
  <a href="/projects">
    <p class="text-xl">Projects</p>
  </a>
  <a href="/contact">
    <p class="text-xl">Contact</p>
  </a>
</div>
{@render children()}
