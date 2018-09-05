This project helps you build a custom theme for NativeChat webchat.

## Prerequisites 

You need to have node.js and git installed locally.

## Creating your theme

1. Clone this repo to a folder on your drive
1. Run `npm install`
1. Go to <https://themebuilder.telerik.com/kendo-react-ui>
1. Click *Start theming* option
1. Choose the *Bootstrap* option when asked to select base theme and then hit *Create* button
1. Customize the colors to match your needs.
1. Click the *Download* button in the top right corner of the screen to download your theme
1. Unzip the downloaded archive
1. Open the `variables.scss` file and copy its contents
1. Find the `public/scss/_custom.scss` file in this repo and paste the contents of variables.scss, overwriting its current contents
1. Run the `npm run build` command
1. Find the generated CSS file in `build/static/css` folder
1. Save the generated CSS file somewhere on your website
1. Configure the webchat by adding the following Setting:

```javascript
var chatSettings = {
  ...
  css: [
    'https://path-to-the-css-file-on-your-webserver'
  ],
  ...
};
```