<script lang="ts">
	let props = { ...$$restProps };
	export let noPadding = false;
	let withPadding = true;
	if (noPadding) {
		withPadding = false;
	}
</script>
		<div class="rounded-2xl shadow-xl {props.class}" class:noPadding class:withPadding>
			<slot />
		</div>
<style>
	.noPadding {
		@apply px-1 py-2;
	}
	.withPadding {
		@apply px-8 py-12 sm:px-12 lg:px-8;
	}
</style>
