<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Headerone from "./Headerone.svelte";
</script>

<Meta
  title="H1"
  component={Headerone}
  argTypes={{
    label: { control: "text" },
    primary: { control: "boolean" },
    backgroundColor: { control: "color" },
    fontColor: { control: "color" },
    size: {
      control: { type: "select", options: ["mobile", "standard", "mega"] },
    },
  }}
/>

<Template let:args>
  <Headerone
    {...args}
  />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
    label: "Header 1",
  }}
/>
<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Header 1",
  }}
/>
