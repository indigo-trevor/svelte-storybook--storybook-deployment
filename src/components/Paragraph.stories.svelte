<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Paragraph from "./Paragraph.svelte";
</script>

<Meta
  title="P"
  component={Paragraph}
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
  <Paragraph
    {...args}
  />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
    label: "Paragraph text primary",
  }}
/>
<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Paragraph text secondary",
  }}
/>
