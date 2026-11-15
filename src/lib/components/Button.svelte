<script lang="ts">
  // Props
  let {
    href,
    children,
    ...restProps
  } = $props()
</script>

{#if href}
  <a {href} {...restProps}>
    {@render children?.()}
  </a>
{:else}
  <button {...restProps}>
    {@render children?.()}
  </button>
{/if}