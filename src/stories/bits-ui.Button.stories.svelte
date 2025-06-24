<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
	import {Button as BitsUIButton} from 'bits-ui';

  const Button = BitsUIButton.Root;

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Bits-UI/Button',
    component: Button,
    tags: ['autodocs'],
  });
</script>

<Button title="Test Button" class="bg-blue-500 text-white p-2 rounded">
  Test button
</Button>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Default">
  Test button
</Story>
