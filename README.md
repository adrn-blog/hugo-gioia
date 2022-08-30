
# Gioia

Gioia is simple and minimalist theme for blogs and personal websites based on
[Goa](https://github.com/kaapiandcode/hugo-goa).

<img src="https://i.imgur.com/vqMd1Mx.png" width="40%" height="40%" />

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/adrn-blog/hugo-gioia/main/LICENSE)

## Installation

From the root of your blog:

```
mkdir -p themes
cd themes
git clone https://github.com/adrn-blog/hugo-gioia
```

## Content creation

### Creating a post

To create a new page or post:

````
hugo new about.md
````
or

````
hugo new posts/first.md
````

You can now go ahead an edit the newly created file under the `content` directory. Once you are finished editing, to have hugo generate the page, set `draft = false` in the articles front matter.

### Organizing pages

The above example demonstrates how to create a pages and posts. Hugo automatically applies the list templates for a directory of pages/posts, which works well for blogs and posts. However, you may want at times want to override this behavior and create a standalone page (like an about page or projects page) or have more control of what content is listed from within the directory. In such cases, you can override the default behavior by placing an index.md file in the corresponding content
directory.

````
hugo new projects/index.md
````

### Page settings

These settings are at the page level.

- `showpagemeta`: default=`true`. This allows you to disable page meta information from being displayed. For example, this setting is disabled [here](https://kaapiandcode.github.io/hugo-goa-demo/about/) and enabled [here](https://kaapiandcode.github.io/hugo-goa-demo/coderag/).
- `showcomments`: default=`true`. Enables or disable comments. For example, this setting is disabled [here](https://kaapiandcode.github.io/hugo-goa-demo/blog/third/) and enabled [here](https://kaapiandcode.github.io/hugo-goa-demo/blog/first/).

## Configuration

The provided
[config.toml](https://github.com/adrn-blog/hugo-gioia/blob/main/exampleSite/config.toml)
describes all options and features that are supported. Configure it your way!

### Basic Configuration

These are site wide configuration parameters that are used by this template.

- `baseurl`: This is the root of your site.
- `builddrafts`: default=`false`. Enables or Disable building drafts when hugo is run.
- `canonifyurls`: default=`false`. Prefix all relative URLs with your base URL. [More Information](https://gohugo.io/extras/urls#canonicalization).
- `languageCode`: Used to set site localization preferences. eg. `en-US`.
- `contentdir`: Where hugo can find your content. eg. `content`.
- `layoutdir`: Where hugo can find your templates. eg. `layouts`.
- `publishdir`: Where hugo generates the static site. eg. `public`.
- `author`: Site author name. eg. `Erlich Bachman`.
- `title`: Site title name. eg. `Erlich Bachman`.
- `theme`: Your theme name should be set to `hugo-goa` if using this theme.

## Hugo Built-in Features

These are features that hugo provides and are used by this template.

- `disqusShortname`: Your discusShortname if you want to enable comments on your posts.
- `googleAnalytics`: Your google analytics id for tracking.
- `enableRobotsTXT`: Enable or disable search engines from crawling your site.

## Site Settings `[params]`

These are settings that are specific to this theme.

- `author`: Main author name. eg. `Erlich Bachman`.
- `intro`: Author introduction. This field supports markdown. eg. `Startup Guru Extraordinaire`.
- `description`: Author description. This field supports markdown. eg. `Now @Pied Piper. Previously @Hacker Hostel, @Bachmanity and @Aviato. <br/> \"What is F times 5? It's Fleventy-five.\"`.
- `authorimage`: Location of author image under static/img directory. eg. `headshot.jpg`
- `dateformat`: Golang date format to be used on this site. eg. `Jan 2, 2006`

### Site Meta Settings `[params.meta]`

These settings are included in the site's meta section.

- `description`: User this field to describe your site to search engines. eg. `Simple minimalist theme`.
- `keywords`: Keywords that desribe your site. eg. `minimalist,blog,goa,hugo,developer`.

### Social Accounts `[params.social]`

These settings to display your social accounts.

- `github`: Your [Github](https://github.com) username.
- `instagram`: Your [Instagram](https://www.instagram.com) username.
- `xing`: Your [Xing](https://www.xing.com) username.
- `linkedin`: Your [Linkedin](https://www.linkedin.com) username.
- `twitter`: Your [Twitter](https://twitter.com) username.
- `facebook`: Your [Facebook](https://www.facebook.com) username.
- `google`: Your [Google](https://www.google.com) username.
- `googlescholar`: Your [Google Scholar](https://scholar.google.com) account ID. [How to get this ID](#google-scholar)
- `medium`: Your [Medium](https://medium.com) username.
- `devto`: Your [dev.to](https://dev.to) username.
- `stackoverflow`: Your [StackOverflow](https://stackoverflow.com) username.
- `angellist`: Your [AngelList](https://angel.co) username.
- `lastfm`: Your [Last.fm](https://www.last.fm) username.
- `goodreads`: Your [Goodreads](https://www.goodreads.com) username.
- `gitlab`: Your [Gitlab](https://gitlab.com) username.
- `bitbucket`: Your [BitBucket](https://bitbucket.org) username.
- `fivehundredpx`: Your [500px](https://500px.com) username.
- `flickr`: Your [Flickr](https://flickr.com) username.
- `foursquare`: Your [Foursquare](https://foursquare.com) username.
- `hackernews`: Your [Y Combinator Hackernews](https://news.ycombinator.com) username.
- `kickstarter`: Your [Kickstarter](https://kickstarter.com) username.
- `patreon`: Your [Patreon](https://patreon.com) username.
- `pintrest`: Your [Pintrest](https://pintrest.com) username.
- `steam`: Your [Steam](https://steamcommunity.com) username.
- `reddit`: Your [Reddit](https://www.reddit.com) username.
- `snapchat`: Your [Snapchat](https://snapchat.com) username.
- `keybase`: Your [Keybase](https://keybase.io) username.
- `twitch`: Your [Twitch](https://twitch.tv) username.
- `youtube`: Your [YouTube](https://youtube.com) channel ID.
- `soundcloud`: Your [Soundcloud](https://soundcloud.com) username.
- `tumblr`: Your [Tumblr](https://tumblr.com) username.
- `strava`: Your [Strava](https://strava.com) username.
- `skype`: Your [skype](https://skype.com) username.
- `telegram`: Your [Telegram](https://telegram.com) username.
- `whatsapp`: Your phone number. Follow the steps [here](https://faq.whatsapp.com/en/26000030/). [Privacy Warning](#privacy-warning)
- `email`: Your email. [Privacy Warning](#privacy-warning)
- `pgp`: Your PGP key. The value should be set to the key fingerprint, and the public key should pe placed in static/key_fingerprint.txt

#### Privacy Warning
It is recommended to keep your private data (phone number/ email) private. Especially if you don't use them for business. Adding it to your public will expose your data to the public. This is irreversible.

#### Account Details
##### Google Scholar
To get this ID, go to Google Scholar, press the "My Profile" tab at the top, then copy the text after the `user=` till the first subsequent `&` (e.g. the `ACCOUNT_ID` part in `https://scholar.google.com/citations?user=ACCOUNT_ID&hl=en`).

### Extras `[params.extra]`

These settings for extra features that this site uses.

- `copyright`: Add a copyright statement to the bottom of the theme. eg. `© 2016. Erlich Bachman. [Some Rights Reserved](https://creativecommons.org/licenses/by/3.0/)."`
- `rss`: Enable rss icon next to social accounts.
- `poweredby`: Help promote this theme and give the authors credit. eg. `true` or `false`.
- `highlightjs`: Use highlightJS to highlight code on your site. eg. `true` or `false`.
- `socialmarkup`: Adds links that conform to the [Schema.org](schema.org) markup. See this [link](https://developers.google.com/search/docs/data-types/social-profile) for more.

### Main Menu `[[menu.main]]`

These settings for the main menu that is displayed on the home page.

- `name`: Name of menu item. eg. `blog`
- `weight`: Weight of this menu item. Higher items go to the bottom. eg. `100`
- `url`: Root URL for this section/page. eg. `/blog/`.

Example:
```toml
[[menu.main]]
    name = "blog"
    weight = 100
    url = "/blog/"
[[menu.main]]
    name = "about"
    weight = 200
    url = "/about/"
[[menu.main]]
    name = "coderag"
    weight = 300
    url = "/coderag/"
```

## Attribution

This is a fork of [Goa](https://github.com/kaapiandcode/hugo-goa).

## License

Licensed under the [MIT](https://opensource.org/licenses/MIT) License. See the
[LICENSE](https://raw.githubusercontent.com/adrn-blog/hugo-gioia/main/LICENSE) file for
more details.
