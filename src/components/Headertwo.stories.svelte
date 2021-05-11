<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Headertwo from "./Headertwo.svelte";
</script>

<Meta
  title="H2"
  component={Headertwo}
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
  <Headertwo
    {...args}
  />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
    label: "Header 2",
  }}
/>
<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Header 2",
  }}
/>
