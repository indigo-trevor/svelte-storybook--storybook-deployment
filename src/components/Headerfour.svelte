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

    let mode = primary ? 'c-h4--primary' : 'c-h4--secondary';

    let style = `color: ${fontColor};` + `background-color: ${backgroundColor};`;

  </script>

  <h4 class={['c-h4', `c-h4--${size}`, mode].join(' ')}
      {style}>
      {label}
  </h4>

  <style lang="scss">
    h4 {
        font-family: "Helvetica Neue",Arial,sans-serif;
        font-size: 1em;
        font-weight: 800;
        margin: 0 0;
        text-transform: uppercase;
        &.c-h4 {
            &--primary {
                color: #333333;
            }
            &--secondary {
                color: #fff;
                background-color:#333333;
            }
            &--mobile {
                font-size: .9em;
            }
            &--mega {
                font-size: 1.1em;
            }
        }
    }
  </style>

