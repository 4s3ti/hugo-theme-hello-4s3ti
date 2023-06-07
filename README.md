# Hello Friend 4s3ti

[![semantic-release: angular](https://img.shields.io/badge/semantic--release-angular-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

![Hello Friend 4s3ti](images/screenshot.png)

## General informations

This theme is a mix between [hello-friend-ng](https://github.com/rhazdon/hugo-theme-hello-friend-ng) and the original [hello-friend](https://github.com/panr/hugo-theme-hello-friend) considering both have features I like and lack others, I've decided to roll up my sleeve and tweak it a bit, the biggest change is most likely a dependency on fontawesome kits. 

You can see it in action here: https://4s3ti.net

---

## Table of Contents

- [Features](#features)
- [How to start](#how-to-start)
- [How to configure](#how-to-configure)
- [More](#more-things)
  - [Built in shortcodes](#built-in-shortcodes)
    - [image](#image)
  - [Code highlighting](#code-highlighting)
  - [Favicon](#favicon)
  - [Audio Support](#audio-support)
- [Social Icons](#social-icons)
- [Hide Title and Language on single pages](#hide-title-and-language-on-single-pages)
- [Known issues](#known-issues)
- [How to edit the theme](#how-to-edit-the-theme)
- [Changelog](CHANGELOG.md)
- [Sponsoring](#sponsoring)
- [Licence](#licence)

---

## Features

### Original features

- Theming: **dark/light mode**, depending on your system preferences or the users choice
- Great reading experience thanks to [**Inter font**](https://rsms.me/inter/), made by [Rasmus Andersson](https://rsms.me/about/)
- Nice code highlighting thanks to [**PrismJS**](https://prismjs.com)
- An easy way to modify the theme with Hugo tooling
- Fully responsive
- Audio support for posts (thanks to [@talbotp](https://github.com/talbotp))
- Support for [Commento](https://commento.io)

### Changed by this theme

- Support for FontAwesome kits
  - Support for social icons
    - Social Icons can be either in the footer or in the main content area just like the original
  - Support for sharing buttons (Depends on FontAwesome Kits)
- Support for latest posts on front page
- Support for submenus
- Builtin (enable/disable) multilanguage menu
  - Shows Language flags
  - Menu will show alternative languages instead of current language
  - When only 2 languages available no sub-menu will be displayed, it will switch between them instead
- Optional overlay that darkens a bit the Background
- Option to choose between read more in text instead of a button
- Page title can be different than site title
- Option to hide page title in single pages
- Option to hide language selection in Single pages

## How to start

You can download the theme manually by going to [https://github.com/4s3ti/hugo-theme-hello-4s3ti.git](https://github.com/4s3ti/hugo-theme-hello-4s3ti.git) and pasting it to `themes/hello-4s3ti` in your root directory.

You can also clone it directly to your Hugo folder:

``` bash
$ git clone https://github.com/4s3ti/hugo-theme-hello-4s3ti.git themes/hello-4s3ti
```

If you don't want to make any radical changes, it's the best option, because you can get new updates when they are available. To do so, include it as a git submodule:

``` bash
$ git submodule add https://github.com/4s3ti/hugo-theme-hello-4s3ti.git themes/hello-4s3ti
```

## How to configure


The theme doesn't require any advanced configuration. Just copy the following config file.
To see all possible configurations, [check the docs](docs/config.md).

Note: There are more options to configure. Take a look into the `config.toml` and `config.yaml` in [exampleSite](./exampleSite/) directory.

``` toml
baseurl      = "localhost"
title        = "My Blog"
languageCode = "en-us"
theme        = "hello-4s3ti"
paginate     = 10

[params]
  dateform        = "Jan 2, 2006"
  dateformShort   = "Jan 2"
  dateformNum     = "2006-01-02"
  dateformNumTime = "2006-01-02 15:04"

  # Subtitle for home
  homeSubtitle = "A simple and beautiful blog"

  # Set disableReadOtherPosts to true in order to hide the links to other posts.
  disableReadOtherPosts = false

  # Enable sharing buttons, if you like
  enableSharingButtons = true

  # Metadata mostly used in document's head
  description = "My new homepage or blog"
  keywords = "homepage, blog"
  images = [""]

[taxonomies]
    category = "blog"
    tag      = "tags"
    series   = "series"

[languages]
  [languages.en]
    title = "Hello Friend NG"
    subtitle = "A simple theme for Hugo"
    keywords = ""
    copyright = '<a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank" rel="noopener">CC BY-NC 4.0</a>'
    readOtherPosts = "Read other posts"

    [languages.en.params.logo]
      logoText = "hello friend ng"
      logoHomeLink = "/"
    # or
    #
    # path = "/img/your-example-logo.svg"
    # alt = "Your example logo alt text"

  # And you can even create generic menu
  [[menu.main]]
    identifier = "blog"
    name       = "Blog"
    url        = "/posts"
```

## More things

### Built-in shortcodes

Of course you are able to use all default shortcodes from hugo (https://gohugo.io/content-management/shortcodes/).

#### image

Properties:

  - `src` (required)
  - `alt` (optional)
  - `position` (optional, default: `left`, options: [`left`, `center`, `right`])
  - `style`

Example:

``` golang
{{< image src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" >}}
```

### Code highlighting

By default the theme is using PrismJS to color your code syntax. All you need to do is to wrap you code like this:

<pre>
``` html
  // your code here
```
</pre>

### Favicon

Check the [docs](docs/favicons.md).

### Audio Support

You wrote an article and recorded it? Or do you have a special music that you would like to put on a certain article? Then you can do this now without further ado.

In your article add to your front matters part:

```yaml
audio: path/to/file.mp3
```

## Social Icons:

### FontAwesome

To use the Social Media icons and the Share Icons you are required to have at least a free [FontAwesome](https://fontawesome.com) Icon Kit   

* Go to [FontAwesome](https://fontawesome.com)
* Create an account
* Go to kits, create new kit
* Add the Kit Link to your config


A large variety of social icons are available and can be configured like this:

```toml
[[params.social]]
  name = "<site>"
  url = "<profile_URL>"
```
If the icon is not available or you wish to use another icon, you can also override the icon by specifying the Icon value.

```toml
[[params.social]]
  name = "<site>"
  url = "<profile_URL>"
  icon = "<Icon>"
```
### Hide Title and Language on single pages


```toml
+++
Title = "Ferramentas"
hideTitle = true
hidelanguage = true
+++
```

## How to edit the theme

Just edit it. You don't need any node stuff. ;)

## Sponsoring

If you like this fork and think it is worth your support, you can always ...  <br />
<a href="https://www.buymeacoffee.com/4s3ti" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-green.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" ></a>

However, please consider doing it to the guys that did most of the hard work, I only moved some bits of code here and there<br />

| [djodjeatlialp](https://github.com/rhazdon/hugo-theme-hello-friend-ng) | [panr](https://github.com/panr/hugo-theme-hello-friend) |
----------------|------|
| <a href="https://www.buymeacoffee.com/djordjeatlialp" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-green.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" ></a> | <a href="https://www.buymeacoffee.com/panr" target="_blank"><img src="https://res.cloudinary.com/panr/image/upload/v1579374705/buymeacoffee_y6yvov.svg" alt="Buy Me A Coffee" ></a>

## Licence

The theme is released under the MIT License. Check the [original theme license](https://github.com/rhazdon/hugo-theme-hello-friend-ng/blob/master/LICENSE.md) for additional licensing information.
