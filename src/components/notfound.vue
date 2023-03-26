<template>
<html>
        <head>
        <title>ecommerce catalog</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta charset="utf-8" />
        <meta property="twitter:card" content="summary_large_image" />
    
        <link
          rel="stylesheet"
          href="https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&amp;display=swap"
          data-tag="font"
        />
        <link rel="stylesheet" href="./style.css" />
      </head>
      <body>
        <div>
          <link href="./page-unavailableproduct.css" rel="stylesheet" />
    
          <div class="page-unavailableproduct-container">
            <div class="page-unavailableproduct-page-unavailableproduct">
              <img
                alt="Rectangle52429"
                src="playground_assets/rectangle52429-z7pb-2000w.png"
                class="page-unavailableproduct-rectangle5"
              />
              <img
                alt="Rectangle72438"
                src="playground_assets/rectangle72438-xquc-1100w.png"
                class="page-unavailableproduct-rectangle7"
              />
              <div class="page-unavailableproduct-sadface">
                <span class="page-unavailableproduct-text">:</span>
                <span class="page-unavailableproduct-text1"> ( </span>
              </div>
              <div class="page-unavailableproduct-group22">
                <span class="page-unavailableproduct-text2">
                  This product is unavailable to show
                </span>
                <div class="page-unavailableproduct-group21">
                  <span class="page-unavailableproduct-text3">Refresh the page to go back</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </body>
</html>
    
    
</template>
    
<script>

    
export default {
      name: 'NotFoundPage',
      props: {
        msg: String
      }
    }
    
</script>
    
<style data-tag="reset-style-sheet">
         html {  line-height: 1.15;}body {  margin: 0;}* {  box-sizing: border-box;  border-width: 0;  border-style: solid;}p,li,ul,pre,div,h1,h2,h3,h4,h5,h6,figure,blockquote,figcaption {  margin: 0;  padding: 0;}button {  background-color: transparent;}button,input,optgroup,select,textarea {  font-family: inherit;  font-size: 100%;  line-height: 1.15;  margin: 0;}button,select {  text-transform: none;}button,[type="button"],[type="reset"],[type="submit"] button::-moz-focus-inner,[type="button"]::-moz-focus-inner,[type="reset"]::-moz-focus-inner,[type="submit"]::-moz-focus-inner {  border-style: none;  padding: 0;}button:-moz-focus,[type="button"]:-moz-focus,[type="reset"]:-moz-focus,[type="submit"]:-moz-focus {  outline: 1px dotted ButtonText;}a {  color: inherit;  text-decoration: inherit;}input {  padding: 2px 4px;}img {  display: block;}html { scroll-behavior: smooth  }
</style>
    
<style data-tag="default-style-sheet">
        html {
            font-family: Inter;
            font-size: 16px;
        }
    
          body {
            font-weight: 400;
            font-style:normal;
            text-decoration: none;
            text-transform: none;
            letter-spacing: normal;
            line-height: 1.15;
            color: var(--dl-color-gray-black);
            background-color: var(--dl-color-gray-white);
    
          }
    
          .page-unavailableproduct-container {
      min-height: 100vh;
    }
    .page-unavailableproduct-page-unavailableproduct {
      width: 100%;
      height: 1011px;
      display: flex;
      overflow: hidden;
      position: relative;
      align-items: flex-start;
      flex-shrink: 0;
      border-color: transparent;
      background-color: rgba(255, 255, 255, 1);
    }
    .page-unavailableproduct-rectangle5 {
      top: 0px;
      left: -5px;
      width: 1921px;
      height: 624px;
      position: absolute;
      border-color: transparent;
    }
    .page-unavailableproduct-rectangle7 {
      top: 0px;
      left: 0px;
      right: 0px;
      width: 1034px;
      bottom: 0px;
      height: 580px;
      margin: auto;
      position: absolute;
      border-color: transparent;
      border-radius: 10px;
    }
    .page-unavailableproduct-sadface {
      top: 247px;
      left: 425px;
      width: 1028px;
      height: 439px;
      display: flex;
      padding: 0;
      position: absolute;
      align-self: auto;
      box-sizing: border-box;
      align-items: flex-start;
      flex-shrink: 1;
      border-color: transparent;
      border-style: none;
      border-width: 0;
      margin-right: 0;
      border-radius: 0px 0px 0px 0px;
      margin-bottom: 0;
      flex-direction: row;
      justify-content: flex-start;
      background-color: transparent;
    }
    .page-unavailableproduct-text {
      top: -59px;
      left: 415px;
      color: rgba(0, 0, 0, 0.10000000149011612);
      height: auto;
      margin: auto;
      position: absolute;
      font-size: 450px;
      align-self: auto;
      font-style: Regular;
      text-align: left;
      font-family: Inter;
      font-weight: 400;
      line-height: normal;
      font-stretch: normal;
      text-decoration: none;
    }
    .page-unavailableproduct-text1 {
      top: -21px;
      left: 502px;
      color: rgba(0, 0, 0, 0.1);
      width: auto;
      height: auto;
      margin: auto;
      position: absolute;
      font-size: 450px;
      max-width: var(--dl-size-size-medium);
      min-width: auto;
      align-self: auto;
      font-style: Regular;
      text-align: left;
      font-family: Inter;
      font-weight: 400;
      line-height: normal;
      font-stretch: normal;
      text-decoration: none;
    }
    .page-unavailableproduct-group22 {
      top: 481px;
      left: 708px;
      width: 465px;
      height: 79px;
      margin: auto;
      display: flex;
      padding: 0;
      position: absolute;
      align-self: auto;
      box-sizing: border-box;
      align-items: flex-start;
      flex-shrink: 1;
      border-color: transparent;
      border-style: none;
      border-width: 0;
      margin-right: 0;
      border-radius: 0px 0px 0px 0px;
      margin-bottom: 0;
      flex-direction: row;
      justify-content: flex-start;
      background-color: transparent;
    }
    .page-unavailableproduct-text2 {
      top: -10px;
      color: rgb(0, 0, 0);
      right: 50px;
      height: auto;
      margin: auto;
      position: absolute;
      font-size: 20px;
      align-self: auto;
      font-style: Regular;
      text-align: left;
      font-family: Inter;
      font-weight: 400;
      line-height: normal;
      font-stretch: normal;
      text-decoration: none;
    }
    .page-unavailableproduct-group21 {
      top: 0px;
      left: 0px;
      right: 0px;
      width: 465px;
      bottom: 0px;
      height: 42px;
      margin: auto;
      display: flex;
      padding: 0;
      position: absolute;
      align-self: auto;
      box-sizing: border-box;
      align-items: flex-start;
      flex-shrink: 1;
      border-color: var(--dl-color-gray-500);
      border-style: solid;
      border-width: 1px;
      border-radius: 0px 0px 0px 0px;
      flex-direction: row;
      justify-content: flex-start;
      background-color: #ffffff;
    }
    .page-unavailableproduct-text3 {
      top: 9px;
      left: 96px;
      color: rgb(62, 62, 62);
      height: auto;
      position: absolute;
      font-size: 20px;
      align-self: auto;
      font-style: Semi Bold;
      text-align: left;
      font-family: Inter;
      font-weight: 700;
      line-height: normal;
      font-stretch: normal;
      text-decoration: none;
    }
    
    :root {
      --dl-color-gray-500: #595959;
      --dl-color-gray-700: #999999;
      --dl-color-gray-900: #D9D9D9;
      --dl-size-size-large: 144px;
      --dl-size-size-small: 48px;
      --dl-color-danger-300: #A22020;
      --dl-color-danger-500: #BF2626;
      --dl-color-danger-700: #E14747;
      --dl-color-gray-black: #000000;
      --dl-color-gray-white: #FFFFFF;
      --dl-size-size-medium: 96px;
      --dl-size-size-xlarge: 192px;
      --dl-size-size-xsmall: 16px;
      --dl-space-space-unit: 16px;
      --dl-color-primary-100: #003EB3;
      --dl-color-primary-300: #0074F0;
      --dl-color-primary-500: #14A9FF;
      --dl-color-primary-700: #85DCFF;
      --dl-color-success-300: #199033;
      --dl-color-success-500: #32A94C;
      --dl-color-success-700: #4CC366;
      --dl-size-size-xxlarge: 288px;
      --dl-size-size-maxwidth: 1400px;
      --dl-radius-radius-round: 50%;
      --dl-space-space-halfunit: 8px;
      --dl-space-space-sixunits: 96px;
      --dl-space-space-twounits: 32px;
      --dl-radius-radius-radius2: 2px;
      --dl-radius-radius-radius4: 4px;
      --dl-radius-radius-radius8: 8px;
      --dl-space-space-fiveunits: 80px;
      --dl-space-space-fourunits: 64px;
      --dl-space-space-threeunits: 48px;
      --dl-space-space-oneandhalfunits: 24px;
    }
    .button {
      color: var(--dl-color-gray-black);
      display: inline-block;
      padding: 0.5rem 1rem;
      border-color: var(--dl-color-gray-black);
      border-width: 1px;
      border-radius: 4px;
      background-color: var(--dl-color-gray-white);
    }
    .input {
      color: var(--dl-color-gray-black);
      cursor: auto;
      padding: 0.5rem 1rem;
      border-color: var(--dl-color-gray-black);
      border-width: 1px;
      border-radius: 4px;
      background-color: var(--dl-color-gray-white);
    }
    .textarea {
      color: var(--dl-color-gray-black);
      cursor: auto;
      padding: 0.5rem;
      border-color: var(--dl-color-gray-black);
      border-width: 1px;
      border-radius: 4px;
      background-color: var(--dl-color-gray-white);
    }
    .list {
      width: 100%;
      margin: 1em 0px 1em 0px;
      display: block;
      padding: 0px 0px 0px 1.5rem;
      list-style-type: none;
      list-style-position: outside;
    }
    .list-item {
      display: list-item;
    }
    .teleport-show {
      display: flex !important;
      transform: none !important;
    }
    .Heading {
      font-size: 32px;
      font-family: Inter;
      font-weight: 700;
      line-height: 1.15;
      text-transform: none;
      text-decoration: none;
    }
    .Content {
      font-size: 16px;
      font-family: Inter;
      font-weight: 400;
      line-height: 1.15;
      text-transform: none;
      text-decoration: none;
    }
    
</style>