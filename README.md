# XMB Menu for ES-DE

This is a translation of the PSP XMB menu for ES-DE. The xml and images were originally built by InitialDin and I've done a refactor to clean up image assets, add color scheme support, customizations and additional aspect ratios. This repository will maintain our shared work so that it can be used with ES-DE's theme downloader.

## **Preview**

![Preview](https://github.com/user-attachments/assets/77926f1b-1f0c-4a21-873a-b7191ce26c31)

## **Configuration Options**

- The theme has a simple set of options that can be changed directly from the UI Settings menu of ES-DE 
- `Theme Variant` - Sets the layout used for the gamelist view when media & metadata are scraped for your games.  There are 4 variants to choose from:
   - `Carousel: Boxart` - A simple carousel that displays game cover artwork
   - `Carousel: Marquee` - A simple carousel that displays game marquee artwork
   - `Carousel: Title Screen` - A simple carousel that displays game title screens
   - `Carousel: Physical Media` - A simple carousel that displays game physical media
- `Theme Color Scheme` - Sets the color scheme, system artwork and system logo used on all views.  This can be customized by following the instructions in the [Customizations](#customizations) section below.
- `Theme Font Size` - Sets the font size to use. I've included font sizes built to scale well from small handheld screens all the way up through larger tv screens.
- `Theme Aspect Ratio` - Sets the aspect ratio that the theme will render at. This should happen automatically but if needed, this can be changed manually to match the aspect ratio of your screen.  16:9, 16:10, 4:3, 3:2, 8:7, 20:9 and 1:1 are supported

### **Built-in Color Schemes**

<table>
   <tr>
      <td><img src="https://github.com/user-attachments/assets/77926f1b-1f0c-4a21-873a-b7191ce26c31"/></td>
      <td><img src="https://github.com/user-attachments/assets/ad8b41a9-a561-41c9-b8eb-2751417640b8"/></td>
      <td><img src="https://github.com/user-attachments/assets/f66de94a-09de-43e9-ae5e-e643b5f1ea60"/></td>
   </tr>
   <tr>
      <td><img src="https://github.com/user-attachments/assets/bae1eb32-3ceb-4bd8-a5a9-d7cc85e5fe57"/></td>
      <td><img src="https://github.com/user-attachments/assets/119dcf12-6b6f-448f-a173-398a7e8d7121"/></td>
      <td><img src="https://github.com/user-attachments/assets/c48b276c-4e3a-499b-af8a-4f3182166f9f"/></td>
   </tr>
   <tr>
      <td><img src="https://github.com/user-attachments/assets/7fa3187b-4330-4cce-bb3b-a1d390358037"/></td>
      <td><img src="https://github.com/user-attachments/assets/ddca37a8-1538-45f7-9c60-85f16b7edbcb"/></td>
      <td><img src="https://github.com/user-attachments/assets/6c906b31-1461-4a8d-b97b-b506723f6dca"/></td>
   </tr>
</table>

## **Customizations**

### **Creating your own color scheme**

A custom color scheme lets you to modify any of the colors and backgrounds used in the theme while also allowing you to continue to get updates from the theme downloader.

#### Instructions:

1) In the resources folder you will find a template file called [colors.xml](https://github.com/anthonycaccese/xmb-menu-es-de/blob/main/resources/custom.xml)

2) Make a folder named in the XMB Menu folder called `theme-customizations` and place a copy of the `custom.xml` file inside that folder.  The folder structure should look like this when you are done:
   ```
   /ES-DE/themes/xmb-menu-es-de/theme-customizations/custom.xml
   ```

3) Edit the properites in `custom.xml` to create your custom color scheme.  All properties are optional so you only need to include the properties you actually change.  Any others can be removed and will fallback automatically to defaults.
   - Here is a definition of each property:
      - `iconColor` - Sets the color of icons used across the theme
      - `textColor` - Sets the color of text used across the theme
      - `lineColor` - Sets the color of the line that is shown in the middle of the screen
      - `backgroundImagePath` - Sets the path to the image you would like to display as your background 
      - `backgroundVideoPath` - If you have `showBackgroundVideo` set to true then this sets the path to the video you would like to display as your background
      - `backgroundImageTile` - If you would like to set a solid color background instead of an image then set this to `true` and set `backgroundImagePath` to `${spacerImage`
      - `backgroundColor` & `backgroundColorEnd` - sets the colors to use for the background image and video.  If you would like a gradient then set a different hex value for each and if you would like one solid color then set the same hex value for each.
      - `backgroundGradientType` - if you set a gradient then this sets the direction the gradient will display as.  Options are: `horizontal`, `vertical`
      - `backgroundGameArtType` - If you have `showBackgroundGameArtSystemView` or `showBackgroundGameArtGamelistView` set to true then this property sets the type of gameart to display. Options are: `fanart`, `screenshot`
      - `backgroundGameArtSelector` - If you have `showBackgroundGameArtSystemView` then this property sets the query to use for pulling in game art.  Options are: `lastplayed`, `random`
      - `showBackgroundGameArtSystemView` - Sets if you would like to display video backgrounds.  If you set this then make sure to set a value for `backgroundVideoPath`
      - `showBackgroundGameArtSystemView` - Sets if you would like to display game art backgrounds as you scroll through systems on the system view.
      - `showBackgroundGameArtGamelistView` - Sets if you would like to display game art backgrounds as you scroll through games on the gamelist view
    
4) Set the `Theme Color Scheme` in ES-DE's UI Settings menu to `Custom` and you should see your custom color scheme display.  If you see an error check that the paths discussed above are correct and then check that the values you added for each property are correct and well formatted.

## **Credits:**

- Inspired by the design of the Cross Media bar by Sony for the PSP &amp; PS3
- The orignal XML and images for this theme were created by InitialDin

## **License**

Creative Commons CC-BY-NC-SA - https://creativecommons.org/licenses/by-nc-sa/2.0/
You are free to share and adapt this theme as long as you provide attribution back to me (and the above credits) as well share any updates you make under the same licence terms.
