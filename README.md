# Hello Abyss

![Hello Friend NG](https://dsh.re/d914c)
> *(Image is of hello-friend-ng and may not be 100% accurate. See https://abyss.dev for most accurate appearance.)*
## General informations

This theme is a modified version of [hello-friend-ng](https://github.com/rhazdon/hugo-theme-hello-friend-ng) by Djordje Atlialp. Check it out, maybe it will work better for your purposes. If you really like this theme, buy him a coffee.

You can see an example of this theme in use at https://abyss.dev.

---

## Table of Contents

- [Hello Abyss](#hello-abyss)
  - [General informations](#general-informations)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
    - [What hello-abyss changes over hello-friend-ng](#what-hello-abyss-changes-over-hello-friend-ng)
  - [How to start](#how-to-start)
  - [How to configure](#how-to-configure)
  - [More things](#more-things)
    - [Built-in shortcodes](#built-in-shortcodes)
      - [image](#image)
    - [Code highlighting](#code-highlighting)
    - [Favicon](#favicon)
    - [Audio Support](#audio-support)
  - [Social Icons:](#social-icons)
  - [Known issues](#known-issues)
  - [How to edit the theme](#how-to-edit-the-theme)
  - [Sponsoring](#sponsoring)
  - [Licence](#licence)

---

## Features

- Theming: **dark/light mode**, depending on your system preferences or the users choice
- Great reading experience thanks to [**Inter UI font**](https://rsms.me/inter/), made by [Rasmus Andersson](https://rsms.me/about/)
- Nice code highlighting thanks to [**PrismJS**](https://prismjs.com)
- An easy way to modify the theme with Hugo tooling
- Fully responsive
- Audio support for posts (thanks to [@talbotp](https://github.com/talbotp))
- Support for social icons
- Support for sharing buttons
- Support for [Commento](https://commento.io)

### What hello-abyss changes over hello-friend-ng

- Return of the ability to set a default theme for the website that overrides the OS preferences
- Posts use Date instead of Datetime
- CanonicalURL can be overriden to a different domain
- Logo text can be dynamic and change per page
- Minor cosmetic changes in the 404 page
- Possibly other undocumented changes (sorry!), see the commit log

## How to start

You can download the theme manually by going to [https://github.com/abyss/hugo-theme-hello-abyss](https://github.com/abyss/hugo-theme-hello-abyss) and pasting it to `themes/hello-abyss` in your root directory.

You can also clone it directly to your Hugo folder:

``` bash
$ git clone https://github.com/abyss/hugo-theme-hello-abyss.git themes/hello-abyss
```

If you don't want to make any radical changes, it's the best option, because you can get new updates when they are available. To do so, include it as a git submodule:

``` bash
$ git submodule add https://github.com/abyss/hugo-theme-hello-abyss.git themes/hello-abyss
```

## How to configure

The theme doesn't require any advanced configuration. Just copy the following config file.
To see all possible configurations, [check the docs](docs/config.md).
Note: There are more options to configure. Take a look into the `config.toml` in `exampleSite`.

``` toml
baseurl      = "localhost"
title        = "My Blog"
languageCode = "en-us"
theme        = "hello-abyss"
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
    title = "Hello Abyss"
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

A large variety of social icons are available and can be configured like this:

```toml
[[params.social]]
  name = "<site>"
  url = "<profile_URL>"
```

Take a look into this [list](docs/svgs.md) of available icon options.

If you need another one, just open an issue or create a pull request with your wished icon. :)

## Known issues

There is a bug in Hugo that sometimes causes the main page not to render correctly. The reason is an empty taxonomy part.
Related issue tickets: [!14](https://github.com/rhazdon/hugo-theme-hello-friend-ng/issues/14) [!59](https://github.com/rhazdon/hugo-theme-hello-friend-ng/issues/59).

Either you comment it out completely or you write the following in

``` toml
[taxonomies]
  tag      = "tags"
  category = "categories"
```

## How to edit the theme

Just edit it. You don't need any node stuff. ;)

## Sponsoring

If you like my work and if you think this project is worth to support it, just <br />
<a href="https://www.buymeacoffee.com/djordjeatlialp" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-green.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" ></a>

## Licence

The theme is released under the MIT License. Check the [license](LICENSE.md) for additional information.

Copyright © 2021 Craig Reeder

Portions of this software are copyright of their respective authors and released under the MIT license:

Copyright © 2018 Track3<br />
Copyright © 2019 panr<br />
Copyright © 2019-2021 Djordje Atlialp<br />

