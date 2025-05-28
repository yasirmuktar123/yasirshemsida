<!-- src/routes/devblog/+page.svelte -->
<script>
	export let data;
    import { base } from '$app/paths';
</script>
<div class="main-title">
<h1>Devblog</h1>
</div>
<ul>
	{#each data.posts as post}
		<li class="sub-title">
			<a href="{base}/devblog/{post.slug}">
				{post.title} — {post.date}
			</a>
		</li>
	{/each}
</ul>

<style>
	.main-title {
		font-size:4rem;
		text-align:center;
		margin-bottom:1rem;
		transition:transform 0.3s ease;
		text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
	}
	.main-title:hover {
		transform: scale(1.05);
	}
	.sub-title {
		font-size:2rem;
		text-align: center;
		margin-bottom:2rem;
		opacity:0.9;
		transition: all 0.3s ease;
		color:light;
	}
	.sub-title:hover {
		opacity:1;
		transform: scale(1.02);
		color:white;
	}
	
</style>