<script module>
	import Button from '$lib/components/ui/button/button.svelte';
  import { defineMeta } from '@storybook/addon-svelte-csf';
	// Simply importing these significantly increases the start time even though they're
	// basically just wrappers...
	import * as Drawer from '$lib/components/ui/drawer';
	import * as ContextMenu from '$lib/components/ui/context-menu';
	// ...around these. Importing these instead is much faster.
	// import * as DrawerPrimitive from "vaul-svelte";
	// import * as ContextMenuPrimitive from "bits-ui";

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Shadcn/Button',
    component: Button,
    tags: ['autodocs'],
  });
</script>

<!-- Slow -->
<!-- <Drawer.Root></Drawer.Root>
<ContextMenu.Root></ContextMenu.Root> -->
<!-- Fast -->
<!-- <DrawerPrimitive.Drawer.Root></DrawerPrimitive.Drawer.Root>
<ContextMenuPrimitive.ContextMenu.Root></ContextMenuPrimitive.ContextMenu.Root> -->

<Button title="Test Button" class="bg-blue-500 text-white p-2 rounded">
  Test button
</Button>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Default">
  Test button
</Story>
