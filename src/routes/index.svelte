<script lang="ts">
	import Button from '../lib/components/Button/Button.svelte';
	import Card from '../lib/components/Card/Card.svelte';
	import ResponsiveCard from "../lib/components/Card/ResponsiveCard.svelte";
</script>

<div class="h-screen bg-gray-200">
	<Button label="" class="m-4 text-2xl rounded-3xl hover:bg-indigo-800 bg-indigo-200" outline
		>Hiii</Button
	>
	<ResponsiveCard>
	<Card class="bg-green-300">
		<div class="mb-12 space-y-4">
			<h3 class="text-2xl font-semibold text-purple-900">Graphic Design</h3>
			<p class="mb-6">Obcaecati, quam? Eligendi, nulla numquam natus laborum porro at cum, consectetur ullam tempora ipsa iste officia sed officiis! Incidunt ea animi officiis.</p>
			<a href="/" class="block font-medium text-purple-600">Know more</a>
		</div>
	</Card>
	<Card class="bg-indigo-400 mt-1 px-5" noPadding>
		<div class="text-white">hiii</div>
	</Card>
		<Card class="bg-indigo-400 mt-1 px-5" noPadding>
			<div class="text-white">hiii</div>
		</Card>
		<Card class="bg-indigo-400 mt-1 px-5" noPadding>
			<div class="text-white">hiii</div>
		</Card>
	</ResponsiveCard>
</div>
