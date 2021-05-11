<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Loader from "./Loader.svelte";
</script>

<Meta
  title="Loader"
  component={Loader}
  argTypes={{
    primary: { control: "boolean" },
    loadingTrackColor: { control: "color" },
    loaderColor: { control: "color" },
    size: {
      control: { type: "select", options: ["small", "medium", "large"] },
    },
  }}
/>

<Template let:args>
  <Loader {...args} />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
  }}
/>

<Story
  name="Secondary"
  args={{
    primary: false,
  }}
/>

