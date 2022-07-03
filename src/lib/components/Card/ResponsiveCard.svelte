<div class="container m-auto px-6 md:px-12 xl:px-0">
  <div class="mx-auto grid gap-{gap} md:w-3/4 lg:w-full lg:grid-cols-{largeCols}">
    <slot/>
  </div>
</div>


<script>
  export let largeCols = 3
  export let gap = 6
</script>
