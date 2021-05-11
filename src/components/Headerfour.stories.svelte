<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Headerfour from "./Headerfour.svelte";
</script>

<Meta
  title="H4"
  component={Headerfour}
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
  <Headerfour
    {...args}
  />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
    label: "Header 4",
  }}
/>
<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Header 4",
  }}
/>
