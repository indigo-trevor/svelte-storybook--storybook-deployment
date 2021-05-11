<script>
    /**
     * Is this the principal call to action on the page?
     */
    export let primary = false;

    /**
     * What background color to use
     */
    export let loadingTrackColor;
    /**
     * What loader color to use
     */
     export let loaderColor;
    /**
     * How large should the loader be?
     */
    export let size = 'medium';

    let mode = primary ? 'c-loader--primary' : 'c-loader--secondary';

    let style = `border-top-color: ${loadingTrackColor};` + `border-right-color: ${loadingTrackColor};` + `border-bottom-color: ${loadingTrackColor};` + `border-left-color: ${loaderColor}` + ';';

  </script>

  <div class={['c-loader', `c-loader--${size}`, mode].join(' ')}
       {style}></div>

  <style lang="scss">
    .c-loader {
        overflow: hidden;
        display: inline-block;
        border-radius: 50%;
        width: 8em;
        height: 8em;
        margin: 25px 50px 25px 0;
        font-size: 10px;
        position: relative;
        text-indent: -9999em;
        border-top: 1.1em solid rgba(0, 0, 0, 0.1);
        border-right: 1.1em solid rgba(0, 0, 0, 0.1);
        border-bottom: 1.1em solid rgba(0, 0, 0, 0.1);
        border-left: 1.1em solid #125ef7;
        -webkit-transform: translateZ(0);
        -ms-transform: translateZ(0);
        transform: translateZ(0);
        -webkit-animation: spinner 1.1s infinite linear;
        animation: spinner 1.1s infinite linear;
            &:after {
                border-radius: 50%;
                width: 10em;
                height: 10em;
            }
            &--secondary {
                border-top: 1.1em solid rgba(18, 94, 247, 0.1);
                border-right: 1.1em solid rgba(18, 94, 247, 0.1);
                border-bottom: 1.1em solid rgba(18, 94, 247, 0.1);
                border-left: 1.1em solid #333333;
            }
            &--small {
                width: 4em;
                height: 4em;
                border-width: 0.7em;
            }
            &--large {
                width: 12em;
                height: 12em;
                border-width: 1.5em;
            }
        }
        @-webkit-keyframes spinner {
            0% {
                -webkit-transform: rotate(0deg);
                transform: rotate(0deg);
            }
            100% {
                -webkit-transform: rotate(360deg);
                transform: rotate(360deg);
            }
        }
        @keyframes spinner {
            0% {
                -webkit-transform: rotate(0deg);
                transform: rotate(0deg);
            }
            100% {
                -webkit-transform: rotate(360deg);
                transform: rotate(360deg);
            }
        }
  </style>
