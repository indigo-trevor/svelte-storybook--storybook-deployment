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

    let mode = primary ? 'c-p--primary' : 'c-p--secondary';

    let style = `color: ${fontColor};` + `background-color: ${backgroundColor};`;

  </script>

  <p class={['c-p', `c-p--${size}`, mode].join(' ')}
      {style}>
      {label}
  </p>

  <style lang="scss">
    p {
        font-family: "Helvetica Neue",Arial,sans-serif;
        font-size: 1em;
        font-weight: 500;
        margin: 0 0 .75em 0;
        line-height: 1.5em;
        &.c-p {
            &--primary {
                color: #333333;
            }
            &--secondary {
                color: #ffffff;
                background-color: #333333;
            }
            &--mobile {
                font-size: 0.9em;
            }
            &--mega {
                font-size: 1.1em;
            }
        }
    }
  </style>

