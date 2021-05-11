<script>
    /**
     * Is this the principal call to action on the page?
     */
    export let primary = false;
     /**
    * What background color to use
    */
    export let backgroundColor;
    /**
     * What font color to use
     */
     export let fontColor;
    /**
     * How large should the button be?
     */
    export let size = 'standard';
    /**
     * Button contents
     */
    export let label = '';

    let mode = primary ? 'c-h2--primary' : 'c-h2--secondary';

    let style = `color: ${fontColor};` + `background-color: ${backgroundColor};`;

  </script>

  <h2 class={['c-h2', `c-h2--${size}`, mode].join(' ')}
      {style}>
      {label}
  </h2>

  <style lang="scss">
    h2{
        font-family: "Helvetica Neue",Arial,sans-serif;
        font-size: 2.75em;
        font-weight: 800;
        margin: .25em 0;
        &.c-h2 {
            &--primary {
                color: #333333;
            }
            &--secondary {
                color: #fff;
                background-color: #333333;
            }
            &--mobile {
                font-size: 2.25em;
            }
            &--mega {
                font-size: 3.25em;
            }
        }
    }
  </style>

