# Media Widget

This widget embeds image, video, audio and iframe elements wrapped within a figure and optionally with a caption.

The figure will get an appropriate CSS class reflecting the media type (*image*, *video*, *audio* or *iframe*) and, if aligned is set, one of *left* or *right*.

Currently this widget supports setting the attributes *width* and *height* for all media types and *alt* for images. The *controls*(audio and video) and *allowfullscreen* (iframe) are automatically set.

The resulting HTM will be p.e. for an image with a caption

    <figure class="image">
        <img src="/url/to/media" alt="Some Alternative" />
        <figcaption>An image with alternative text, but witout width and height set</figcaption>
    </figure>

## Supported browser APIs

If you provide a browser implementation that uses one of the following browser APIs the _Browse server_ button will appear:

1. [browser](https://ckeditor.com/cke4/addon/browser) 
2. [mediabrowser](https://ckeditor.com/cke4/addon/mediabrowser) 
3. [filebrowser](https://ckeditor.com/cke4/addon/filebrowser)

**This widget itself does not provide any file browser**

The browser plugin (if installed) will be used as the preferred option, when the URL to your browser implementation is configured

    config.mediaBrowser = '/url/to/browser';

Otherwise the mediabrowser plugin (if installed and configured) will be used as the second option, or the filebrowser plugin (if installed) as the third option.

## Usage with browser and mediabrowser plugin

The browser plugin is the prefer

Your browser implementation can currently send following keys with the message:

    {
        src: '...', //required, URL to media
        type: '...' // optional, media type (audio, iframe, image or video)
        alt: '...', // optional, alternative text (currently only used for images)
    }

## Note

Inline media elements are not supported anymore. If you need them, please stick with version [0.20](https://download.ckeditor.com/media/releases/media_0.20.zip) or use another plugin.

## Demo

https://akilli.github.io/rte/ck4

## Minimalistic browser example

https://github.com/akilli/rte/tree/master/browser
