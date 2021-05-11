<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Headerthree from "./Headerthree.svelte";
</script>

<Meta
  title="H3"
  component={Headerthree}
  argTypes={{
    label: { control: "text" },
    primary: { control: "boolean" },
    fontColor: { control: "color" },
    backgroundColor: { control: "color" },
    size: {
      control: { type: "select", options: ["mobile", "standard", "mega"] },
    },
  }}
/>

<Template let:args>
  <Headerthree
    {...args}
  />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
    label: "Header 3",
  }}
/>
<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Header 3",
  }}
/>
