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

    let mode = primary ? 'c-h3--primary' : 'c-h3--secondary';

    let style = `color: ${fontColor};` + `background-color: ${backgroundColor};`;

  </script>

  <h3 class={['c-h3', `c-h3--${size}`, mode].join(' ')}
      {style}>
      {label}
  </h3>

  <style lang="scss">

    h3{
        font-family: "Helvetica Neue",Arial,sans-serif;
        font-size: 1.75em;
        font-weight: 800;
        margin: .25em 0;
        &.c-h3 {
            &--primary {
                color: #333333;
            }
            &--secondary {
                color: #fff;
                background-color: #333333;
            }
            &--mobile {
                font-size: 1.25em;
            }
            &--mega {
                font-size: 2.25em;
            }
        }
    }


  </style>

