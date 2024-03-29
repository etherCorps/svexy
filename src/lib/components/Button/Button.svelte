<script lang="ts">
	import classNames from 'classnames';
	export let href: string = '';
	export let pill: boolean = false;
	export let variant: 'solid' | 'outlined' = 'solid';
	export let size: 'xs' | 'sm' | 'md' | 'lg' | 'xl' = 'md';
	export let color:
		| 'primary'
		| 'secondary'
		| 'tertiary'
		| 'gray'
		| 'danger'
		| 'info'
		| 'warning'
		| 'success' = 'primary';
	export let shadow: boolean = false;
	export let disabled: boolean = false;
	const comProps = { ...$$restProps };
	const colorClasses = {
		solid: {
			primary: 'text-white bg-primary-700 hover:bg-primary-800 focus:ring-primary-200',
			secondary: 'text-white bg-secondary-700 hover:bg-secondary-800 focus:ring-secondary-200',
			tertiary: 'text-white bg-tertiary-700 hover:bg-tertiary-800 focus:ring-tertiary-200',
			dark: 'text-white bg-gray-700 hover:bg-gray-800 focus:ring-gray-200',
			info: 'text-white bg-info-700 hover:bg-info-800 focus:ring-info-200',
			success: 'text-white bg-success-700 hover:bg-success-800 focus:ring-success-200',
			warning: 'text-white bg-warning-700 hover:bg-warning-800 focus:ring-warning-200',
			danger: 'text-white bg-danger-700 hover:bg-danger-800 focus:ring-danger-200'
		},
		outlined: {
			primary:
				'text-primary-700 hover:text-white border border-2 border-primary-700 hover:bg-primary-800 focus:ring-primary-300',
			secondary:
				'text-secondary-700 hover:text-white border border-2 border-secondary-700 hover:bg-secondary-800 focus:ring-secondary-300',
			tertiary:
				'text-tertiary-700 hover:text-white border border-2 border-tertiary-700 hover:bg-tertiary-800 focus:ring-tertiary-300',
			dark: 'text-gray-700 hover:text-white border border-2 border-gray-700 hover:bg-gray-800 focus:ring-gray-300',
			info: 'text-info-700 hover:text-white border border-2 border-info-700 hover:bg-info-800 focus:ring-info-300',
			success:
				'text-success-700 hover:text-white border border-2 border-success-700 hover:bg-success-800 focus:ring-success-300',
			warning:
				'text-warning-700 hover:text-white border border-2 border-warning-700 hover:bg-warning-800 focus:ring-warning-300',
			danger:
				'text-danger-700 hover:text-white border border-2 border-danger-700 hover:bg-danger-800 focus:ring-danger-300'
		},
		soft: {
			primary:
				'bg-primary-300 text-gray-800 hover:bg-primary-800 hover:text-white focus:ring-primary-200',
			secondary:
				'bg-secondary-300 text-gray-800 hover:bg-secondary-800 hover:text-white focus:ring-secondary-200',
			tertiary:
				'bg-tertiary-300 text-gray-800 hover:bg-tertiary-800 hover:text-white focus:ring-tertiary-100',
			dark: 'bg-gray-300 text-gray-800 hover:bg-gray-800 hover:text-white focus:ring-gray-100',
			info: 'bg-info-300 text-gray-800 hover:bg-info-800 hover:text-white focus:ring-info-100',
			success:
				'bg-success-300 text-gray-800 hover:bg-success-800 hover:text-white focus:ring-success-100',
			warning:
				'bg-warning-300 text-gray-800 hover:bg-warning-800 hover:text-white focus:ring-warning-100',
			danger:
				'bg-danger-300 text-gray-800 hover:bg-danger-800 hover:text-white focus:ring-danger-100'
		}
	};

	const shadowClasses = {
		primary: 'shadow-lg shadow-primary-500/50',
		secondary: 'shadow-lg shadow-secondary-500/50',
		tertiary: 'shadow-lg shadow-tertiary-500/50',
		dark: 'shadow-lg shadow-gray-500/50',
		info: 'shadow-lg shadow-info-500/50',
		success: 'shadow-lg shadow-success-500/50',
		warning: 'shadow-lg shadow-warning-500/50',
		danger: 'shadow-lg shadow-danger-500/50'
	};
	const sizeClasses = {
		xs: 'px-3 py-2 text-xs',
		sm: 'px-3 py-2 text-sm',
		md: 'px-5 py-2.5 text-sm',
		lg: 'px-5 py-3 text-base',
		xl: 'px-6 py-3.5 text-base'
	};
'active:text-primary-700 active:border active:border-2 active:border-primary-700'
	$: buttonClasses = classNames(
		'group text-center font-medium focus:ring-2 focus:outline-none ease-in-out transition-all flex items-center',
		colorClasses[variant][color],
		sizeClasses[size],
		shadow && variant != 'soft' && shadowClasses[color],
		pill ? 'rounded-full' : 'rounded-md',
		$$props.class,
		disabled && 'cursor-not-allowed opacity-50',
	);
</script>

{#if href}
	<a {href} {...$$restProps}
		><button {...$$restProps} {disabled} class={buttonClasses} on:click><slot /></button></a
	>
{:else}
	<button type="button" {...$$restProps} {disabled} class={buttonClasses} on:click><slot /></button>
{/if}
