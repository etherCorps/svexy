<script lang="ts">
    export let label = 'Button'
    export let disabled = false
    export let primary = false
    export let outline = false
    export let filled = false
    let props = {...$$restProps}
    console.log(props.class)
</script>
<button
        class="btn {props.class}"
        class:primary
        class:outline
        class:filled
        {disabled}
        style={props.style}
        props
        on:click>
    {label}
</button>

<style>
    .btn {
        @apply inline-block px-6 py-2.5 font-medium leading-tight shadow-md transition duration-150 ease-in-out text-black;}
    .outline {
        @apply border-0 hover:bg-opacity-10 focus:outline-none focus:ring-0 transition duration-150 ease-in-out;
    }
    .filled{
        @apply hover:bg-opacity-5 hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg transition duration-150 ease-in-out;
    }
</style>
