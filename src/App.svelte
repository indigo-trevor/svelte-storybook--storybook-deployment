<script>
  import Headerone from './components/Headerone.svelte';
  import Headertwo from './components/Headertwo.svelte';
  import Headerthree from './components/Headerthree.svelte';
  import Headerfour from './components/Headerfour.svelte';
  import Button from './components/Button.svelte';
  import Paragraph from './components/Paragraph.svelte';
  import Toast from './components/Toast.svelte';
  import Loader from './components/Loader.svelte';
</script>

<!-- use lang="sass" for SASS -->
<style lang="scss">
    :global {
        @import 'global-styles.scss';
    }
</style>

<!-- Header -->
<section class="l-section l-section--header">
    <div class="l-container">
        <div class="c-content-wrapper m-center-aligned">
            <Headerone label="Svelte & Storybook Component Library" backgroundColor="transparent"/>
            <Paragraph label="Built by Trevor Robinson" backgroundColor="transparent"/>
        </div>
    </div>
</section>
<!-- Buttons -->
<section class="l-section l-section--button">
    <div class="l-header">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Headerfour primary label="Buttons"/>
            </div>
        </div>
    </div>
    <div class="l-body">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Button primary label="Primary Button"/>
                <Button primary size="large" label="Large Primary Button"/>
                <Button primary size="small" label="Small Primary Button"/>
                <Button label="Secondary Button"/>
                <Button size="large" label="Large Secondary Button"/>
                <Button size="small" label="Small Secondary Button"/>
            </div>
        </div>
    </div>
</section>
<!-- Typography -->
<section class="l-section l-section--typogrophy">
    <div class="l-header">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Headerfour primary label="Typography"/>
            </div>
        </div>
    </div>
    <div class="l-body">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Paragraph primary label="Paragraph Primary - Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."/>
                <Headerone primary label="Header 1 Primary"/>
                <Headertwo primary label="Header 2 Primary"/>
                <Headerthree primary label="Header 3 Primary"/>
                <Headerfour primary label="Header 4 Primary"/>
            </div>
        </div>
        <div>
        <div class="l-container">
            <div class="c-content-wrapper c-content-wrapper--secondary m-dark">
                <Paragraph label="Paragraph Secondary - Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."/>
                <Headerone label="Header 1 Secondary"/>
                <Headertwo label="Header 2 Secondary"/>
                <Headerthree label="Header 3 Secondary"/>
                <Headerfour label="Header 4 Secondary"/>

            </div>
        </div>
    </div>
</section>
<!-- Toast Notifications -->
<section class="l-section l-section--toast">
    <div class="l-header">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Headerfour primary label="Toast Notifications"/>
            </div>
        </div>
    </div>
    <div class="l-body">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Toast label="Toast Success"/>
                <Toast label="Toast Warning"/>
                <Toast label="Toast Danger"/>
            </div>
        </div>
    </div>
</section>
<!-- Loader -->
<section class="l-section l-section--loader">
    <div class="l-header">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Headerfour primary label="Loaders"/>
            </div>
        </div>
    </div>
    <div class="l-body">
        <div class="l-container">
            <div class="c-content-wrapper">
                <Loader primary size="large"/>
                <Loader primary />
                <Loader primary size="small"/>
                <br>
                <Loader size="large"/>
                <Loader />
                <Loader size="small"/>
            </div>
        </div>
    </div>
</section>
