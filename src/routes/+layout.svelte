<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import '../lib/assets/global.css';
	import { Icon } from 'svelte-icons-pack';

	import { ImNewTab } from 'svelte-icons-pack/im';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="flex flex-2">
	<div class="flex flex-col">
		<ul class="flex-col p-6 **:h-10 **:hover:text-black">
			<li><a href="/">About</a></li>
			<li><a href="/projects">Projects</a></li>
			<li>
				<a href="https://floatsuki.github.io/blog"
					>Blog <Icon src={ImNewTab} size={15} className="inline" />
				</a>
			</li>
		</ul>
	</div>
	<div class="p-6 pt-6">
		{@render children?.()}
	</div>
</div>
