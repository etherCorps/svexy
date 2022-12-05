<script lang="ts">
	import { Button } from '$lib';
	import { ArrowRight } from 'svelte-heros';

	let variants = ['solid', 'outlined', 'soft'];
	let colors = ['primary', 'secondary', 'tertiary', 'dark', 'info', 'warning', 'danger', 'success'];
</script>

<section>
	<div class="grid items-center space-y-14 p-20">
		{#each variants as variant}
			<div class="">
				<h1
					class="mb-5 text-3xl font-bold px-4 py-2 w-max rounded-full text-black capitalize bg-warning-700/70"
				>
					{variant} Buttons
				</h1>
				<div class="flex space-x-2">
					{#each colors as color}
						<Button class="capitalize drop-shadow-md" {variant} {color} shadow
							>{color}
							<ArrowRight
								size="18"
								class="inline-flex items-center justify-center w-4 h-4 ml-2 rounded-full"
							/></Button
						>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</section>

<!--<Avatar name="John Walker" src="https://avatars0.githubusercontent.com/u/6810985?s=460&u=a2a24f33ad8d17377cef8163f596a7fbd1501cd4&v=4" />-->
