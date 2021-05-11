<script>
    import { NotificationDisplay, notifier } from '@beyonk/svelte-notifications'
    /**
     * Button contents
     */
    export let label = '';

    let themes = { // These are the defaults
          danger: '#bb2124',
          success: '#22bb33',
          warning: '#f0ad4e'
      }

      function fireToast () {
          if(label==="Toast Success") {
            notifier.success(label)
          } else if(label==="Toast Warning") {
            notifier.warning(label)
          } else if(label==="Toast Danger") {
            notifier.danger(label)
          }

      }

  </script>
  <NotificationDisplay {themes} />
  <button
    type="button"
    class="c-button c-button--medium c-button--primary"
    on:click={fireToast}>
    {label}
  </button>

  <style lang="scss">
      .c-button {
        font-family: "Helvetica Neue",Arial,sans-serif;
          border: 1px solid #125ef7;
          padding: 8px 35px;
          transition: all 250ms ease;
          cursor: pointer;
          border-radius: 0;
          display: block;
          transform: scale(1);

          &--primary {
              background-color: #125ef7;
              border-color: #125ef7;
              color: #fff;
              &:hover {
                  background-color: darken(#125ef7, 10%);
                  border-color: darken(#125ef7, 10%);
              }
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
