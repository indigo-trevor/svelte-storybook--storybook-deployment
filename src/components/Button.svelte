<script>
  /**
   * Is this the principal call to action on the page?
   */
  export let primary = false;
  /**
   * What text color to use
   */
   export let textColor;
  /**
   * What background color to use
   */
  export let backgroundColor;
  /**
   * What border color to use
   */
   export let borderColor;
  /**
   * How large should the button be?
   */
  export let size = 'medium';
  /**
   * Button contents
   */
  export let label = '';

  let mode = primary ? 'c-button--primary' : 'c-button--secondary';

  let style = `background-color: ${backgroundColor};` + `border-color: ${borderColor}` + ';' + `color: ${textColor}` + ';';

</script>

<button
  type="button"
  class={['c-button', `c-button--${size}`, mode].join(' ')}
  {style}>
  {label}
</button>

<style lang="scss">
    .c-button {
        font-family: "Helvetica Neue",Arial,sans-serif;
        color: #fff;
        border: 1px solid #125ef7;
        padding: 8px 35px;
        transition: all 250ms ease;
        cursor: pointer;
        border-radius: 0;
        display: block;
        &--primary {
            background-color: #125ef7;
            border-color: #125ef7;
            &:hover {
                background-color: darken(#125ef7, 10%);
                border-color: darken(#125ef7, 10%);
            }
        }
        &--secondary {
            background-color: #fff;
            color: #125ef7;
            &:hover {
                background-color: #125ef7;
                color: #fff;
            }
        }
        &--small {
            font-size: .7em;
            padding: 5px 15px;
        }
        &--large {
            font-size: 1.3em;
            padding: 20px 75px;
        }
        &:not(:disabled):focus,
          &:focus {
              background-color: darken(#125ef7, 25%);
              border-color: darken(#125ef7, 25%);
              outline: none;
              color: #fff;
          }
          &:not(:disabled):active,
          &:active {
              background-color: darken(#125ef7, 25%);
              border-color: darken(#125ef7, 25%);
              transform: scale(0.95);
              outline: none;
              color: #fff;
          }
    }

</style>
