<script>
    /**
     * Is this the principal call to action on the page?
     */
    export let primary = false;
    /**
     * What font color to use
     */
     export let fontColor;
    /**
    * What background color to use
    */
    export let backgroundColor;
    /**
     * How large should the button be?
     */
    export let size = 'standard';
    /**
     * Button contents
     */
    export let label = '';

    let mode = primary ? 'c-h1--primary' : 'c-h1--secondary';

    let style = `color: ${fontColor};` + `background-color: ${backgroundColor};`;

  </script>

  <h1 class={['c-h1', `c-h1--${size}`, mode].join(' ')}
      {style}>
      {label}
  </h1>

  <style lang="scss">

    h1{
        font-family: "Helvetica Neue",Arial,sans-serif;
        font-size: 3.35em;
        font-weight: 800;
        margin: 0 0 .25em 0;
        line-height: 1.2em;
        &.c-h1 {
            &--primary {
                color: #333333;
            }
            &--secondary {
                color: #fff;
                background-color: #333333;
            }
            &--mobile {
                font-size: 3em;
            }
            &--mega {
                font-size: 4em;
            }
        }
    }

  </style>

