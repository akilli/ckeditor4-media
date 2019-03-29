# Media Widget

@todo Needs update, the following is not up to date
media public api merged into api plugin

This media widget can embed image, audio, video and iframe elements solely with their corresponding tags or wrapped within a figure element optionally with a caption. 

In case the media element is wrapped within a figure element, this widget will add the CSS class *image*, *audio*, *video* or *iframe* to the figure element. It also supports alignment by setting an appropriate CSS class (*left* or *right*), and the attributes *width*, *height* and *alt*. The *controls*(audio and video) and *allowfullscreen* (iframe) are automatically set.

## Supported browser APIs

If you have installed a file browser that uses the API of the [mediabrowser add-on](https://ckeditor.com/cke4/addon/mediabrowser) or the [filebrowser add-on](https://ckeditor.com/cke4/addon/filebrowser), the _Browse server_ button will appear. This widget itself does not provide any file browser.

Note: This plugin would actually not need any of these APIs, but uses them to allow you to re-use your existing filebrowser implementation. 

### [Browser plugin](https://ckeditor.com/cke4/addon/browser)

default if browser is installed and config.mediaBrowser is set

### [Media Browser plugin](https://ckeditor.com/cke4/addon/mediabrowser)

Second option if mediabrowser is installed

If you use the [mediabrowser add-on](https://ckeditor.com/cke4/addon/mediabrowser), your media browser implementation can currently send following keys with the message:

    {
        src: '...', //required, URL to media
        type: '...' // optional, media type (audio, iframe, image or video)
        alt: 'Alternative text', // optional, alternative text
    }

### [File Browser plugin](https://ckeditor.com/cke4/addon/filebrowser)

Third option

## Demo

https://akilli.github.io/rte/ck4

## Minimalistic browser example

https://github.com/akilli/rte/tree/master/browser
