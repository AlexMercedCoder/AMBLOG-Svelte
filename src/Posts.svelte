<div>

{#each posts as post}
	<div class="post">
		<h1>{post.fields.blogTitle}</h1>
		<p>{post.fields.blogContent}</p>
	</div>
{:else}
	<!-- this block renders when photos.length === 0 -->
	<p>loading...</p>
{/each}

</div>

<script>
import { onMount } from 'svelte';

	let posts = [];

	onMount(async () => {
	const res = await fetch(`https://cdn.contentful.com/spaces/wiothdq64tqj/environments/master/entries?access_token=fbY3krPsiW8hWQ4m7GysjrfCfBdeCP9gBLqh3klbO20`);
	let data = await res.json();
	window.console.log(data);
	posts = data.items;
});
</script>


<style>

.post {width: 80%; padding: 20px; background-color: #ff3e00; color: white;
border-radius: 10px; margin: 20px auto;}
</style>
