<script lang="ts">
	import classNames from 'classnames';

	export let src: string = '';
	export let alt: string = '';
	export let size: 'xs' | 'sm' | 'md' | 'lg' | 'xl' = 'md';
	export let name: string = ';';
	export let border: boolean = false;
	export let rounded: boolean = false;
	export let borderColor:
		| 'primary'
		| 'secondary'
		| 'tertiary'
		| 'gray'
		| 'danger'
		| 'info'
		| 'warning'
		| 'success' = 'primary';
	const sizes = {
		xs: 'w-6 h-6',
		sm: 'w-8 h-8',
		md: 'w-10 h-10',
		lg: 'w-20 h-20',
		xl: 'w-36 h-36'
	};

	let borderColors: {
		primary: 'ring-primary-300';
		secondary: 'ring-secondary-300';
		tertiary: 'ring-tertiary-300';
		dark: 'ring-gray-300';
		info: 'ring-info-300';
		success: 'ring-success-300';
		warning: 'ring-warning-300';
		danger: 'ring-danger-300';
	};
	let avatarClasses;
	$: avatarClasses = classNames(
		rounded ? 'rounded-full' : 'rounded',
		border && `p-1 ring-2 ${borderColors[borderColor]}`,
		sizes[size],
		$$props.class
	);
</script>
