<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Toast from "./Toast.svelte";
</script>

<Meta
  title="Toasts"
  component={Toast}
  argTypes={{
    label: { control: "text" }
  }}
/>

<Template let:args>
  <Toast {...args} />
</Template>

<Story
  name="Success"
  args={{
    label: "Toast Success",
  }}
/>

<Story
  name="Warning"
  args={{
    label: "Toast Warning",
  }}
/>
<Story
  name="Danger"
  args={{
    label: "Toast Danger",
  }}
/>

