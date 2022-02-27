# Hereditor Theme

## Background

The _Hereditor_ theme for [Grav](https://getgrav.org/) is a fork of the [_Mediator_ theme](https://github.com/getgrav/grav-theme-mediator) developed by [Grav Team and contributors](https://github.com/getgrav/grav-theme-mediator/graphs/contributors), which was a port of the [_Mediator_ theme](https://github.com/dirkfabisch/mediator) for [Jekyll](https://jekyllrb.com/) designed by [Dirk Fabisch](https://twitter.com/dirkfabisch), which in turn was inspired by the [_Readium_ theme](https://github.com/starburst1977/readium) for [Ghost](https://ghost.org/) elaborated by by [Sven Read](https://twitter.com/starburst1977).

--------------------------------------------------------------------------------

## Overview

### Features

- Minimal design
- Responsive layout
- Header images in posted articles
- Support of _featured_ posted articles
- Implementation of [FontAwesome](https://github.com/FortAwesome/Font-Awesome) for icons fonts use
- Integration of free and open source improved fonts (WOFF 2.0)

### Supported page types

The _Hereditor_ theme was mainly conceived to craft a simple blog and supports three distinct page types via templates:

- **default**: a template used to display the default blog listing view
- **post**: a full page for displaying a blog post
- **page**: similar to the post template, but without any author information

--------------------------------------------------------------------------------

## Installation

<!--Installing the _Hereditor_ theme can be done in one of two ways. Using the GPM (Grav Package Manager) installation method enables to quickly and easily install the theme with a simple terminal command, while the manual method enables to do so via a `zip` file.

### GPM Installation

The simplest way to install the theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through the system's Terminal (also called _the command line_). From the root of the Grav install type:

```bash
bin/gpm install hereditor
```

This will install the _Hereditor_ theme into your `/user/themes` directory within Grav. Its files can be found under `/your/site/grav/user/themes/hereditor`.-->

### Manual Installation

To install the theme, just download the `zip` version of this repository and unzip it under `/your/site/grav/user/themes`. Then, rename the folder to `hereditor`. These files can be found <!--either--> on [GitHub](https://github.com/gizmecano/grav-theme-hereditor/)<!-- or via [GetGrav.org](http://getgrav.org/downloads/themes)-->.

All the _Hereditor_ theme files should be into the folder `/your/site/grav/user/themes/hereditor`.

--------------------------------------------------------------------------------

## Updating

As development for the _Hereditor_ theme continues, new versions may become available that add additional features and functionality, improve compatibility with newer Grav releases, and generally provide a better user experience. <!--Updating _Hereditor_ is easy, and can be done through Grav's GPM system, as well as manually.-->

<!--### GPM Update

The simplest way to update this theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm). Navigate to the root directory of the Grav install using the system's Terminal (also called _command line_) and type the following:

```bash
bin/gpm update hereditor
```

This command will check the Grav install to see if the _Hereditor_ theme is due for an update. If a newer release is found, it will be asked whether or not proceed to update. To continue, type `y` and hit enter. The theme will automatically update and clear Grav's cache.-->

### Manual Update

Manually updating _Hereditor_ is pretty simple:

- Delete the `your/site/user/themes/hereditor` directory
- Download the new version of the _Hereditor_ theme from <!--either--> [GitHub](https://github.com/gizmecano/grav-theme-hereditor/)<!-- or [GetGrav.org](https://getgrav.org/downloads/themes)-->
- Unzip the `zip` file in `your/site/user/themes` and rename the resulting folder to `hereditor`
- Clear the Grav cache using admin panel or following command:

```bash
bin/grav clear-cache
```

Note that any changes made to any of the files listed under this directory will also be removed and replaced by the new set. Any files located elsewhere (for example a ``YAML`` settings file placed in `user/config/themes`) will remain intact.

--------------------------------------------------------------------------------

## Setup

To set _Hereditor_ as the default theme, the steps to follow are:

- Navigate to `/your/site/grav/user/config`
- Open the `system.yaml` file
- Change the `theme:` setting to `theme: hereditor`
- Save the changes
- Clear the Grav cache using admin panel or following command:

```bash
bin/grav clear-cache
```

Once this is done, the new theme should be available on the frontend. Keep in mind any customizations made to the previous theme will not be reflected as all of the theme and templating information is now being pulled from the `hereditor` folder.

--------------------------------------------------------------------------------

## Configuration

### Website images

Basically, the _Hereditor_ theme is arranged to use two images for the entire website:

1. `logo`: used into default page and to link toward the home page (but also as basic shortcut icon). This image aims to represent the website and should not exceed a size close to 300px × 300px.
2. `author.image`: set as illustration in the mini-bio. This image aims to represent the author of an article and should not exceed a size close to 300px × 300px.

These two images have to be defined in your `/your/site/grav/user/config/site.yaml` file, such as:

```yaml
logo: /user/images/logo.png
author:
  image: /user/images/avatar.png
```

### Article header images

Header images can be used in articles which are based on the **post** template. Any header image has to be declared in the front-matter section of the post, by adding a tag `image` populated with a proper URL to the intented file, such as this code sample (if the image is set in the same folder as the article):

```yaml
image: header-image.jpg
```

### Social links

In order to set social profiles features to be embedded in _Hereditor_ theme configuration, add the following to your `/your/site/grav/user/config/site.yaml` file:

1. `social.icon`: name of the social platform
2. `social.link`: the main URL of the plateform
3. `social.user`: the specific user name on the plateform

```yaml
social:
  - icon: networkname
    link: https://twitter.com/
    user: username
```

--------------------------------------------------------------------------------

## License

The _Hereditor_ theme is free and open source software, distributed under the [MIT License](/LICENSE) version 2 or later. So feel free to to modify this theme to suit your needs.
