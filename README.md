# Trove newspaper images
> Tools for downloading images from Trove's digitised newspapers and gazettes.


## Background and alternatives

There's no reliable way of downloading an image of a Trove newspaper article from the web interface. The image download option produces an HTML page with embedded images, and the article is often sliced into pieces to fit the page.

This package includes tools to download articles as complete JPEG images. If an article is printed across multiple newspaper pages, multiple images will be downloaded – one for each page. It's intended for integration into other tools and processing workflows, or for people who like working on the command line.

If you just want to quickly download an article as an image without installing anything, you can [use this web app](https://glam-workbench.net/trove-newspapers/#save-a-trove-newspaper-article-as-an-image) in the GLAM Workbench. To download images of all articles returned by a search in Trove, you can also use the [Trove Newspaper and Gazette Harvester](https://glam-workbench.net/trove-harvester/).

See the [documentation](https://wragge.github.io/trove_newspaper_images/) for more information.

## Install

`pip install git+https://github.com/wragge/trove_newspaper_images.git`

## Download articles as images

### Use as a library

```python
from trove_newspaper_images.articles import download_images

images = download_images('107024751')
```

    Downloaded: ['nla.news-article107024751-11565831.jpg']


### Use from the command line

Just call `trove_newspaper_images.download` from the command line with an article identifier. You can use the `--output_dir` parameter to specify a directory for the downloaded images. For example:

```shell
trove_newspaper_images.download 107024751 --output_dir images
```

----

Created by [Tim Sherratt](https://timsherratt.org) ([@wragge](https://twitter.com/wragge)) for the [GLAM Workbench](https://glam-workbench.net/).
