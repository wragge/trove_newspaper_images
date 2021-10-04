# Trove newspaper images
> Tools for downloading images from Trove's digitised newspapers and gazettes.


## Install

`pip install git+https://github.com/wragge/trove_newspaper_images.git`

## Use as a library

```python
from trove_newspaper_images.articles import download_images

images = download_images('107024751')
```

    Downloaded: ['nla.news-article107024751-11565831.jpg']


## Use from the command line

Just call `trove_newspaper_images.download` from the command line with an article identifier. You can use the `--output_dir` parameter to specify a directory for the downloaded images. For example:

```shell
trove_newspaper_images.download 107024751 --output_dir images
```

See the [documentation](https://wragge.github.io/trove_newspaper_images/) for more information.

----

Created by [Tim Sherratt](https://timsherratt.org) ([@wragge](https://twitter.com/wragge)) for the [GLAM Workbench](https://glam-workbench.net/).
