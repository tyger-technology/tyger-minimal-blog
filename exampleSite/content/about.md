+++
title = "About"
date = 2018-02-03T14:02:23+11:00
hide_date = true
+++

Tyger Minimal Blog is a minimal, responsive, CSS-only [Hugo](//gohugo.io/) theme that uses [Boostrap 4](//getbootstrap.com/).

## Installation

In your Hugo site `themes` directory, run:

{{< highlight Bash >}}
$ git clone https://github.com/tyger-technology/tyger-minimal-blog/
{{< /highlight >}}

Next, open `config.toml` in the base of the Hugo site and ensure the theme option is set to `tyger-minimal-blog`.

{{< highlight toml >}}
theme = "tyger-minimal-blog"
{{< /highlight >}}

For more information read the official Hugo [setup guide](//gohugo.io/getting-started/installing/).

## Config File Setup

Take a look inside the [`exampleSite`](https://github.com/tyger-technology/tyger-minimal-blog/tree/master/exampleSite) folder of this theme. You'll find a file called [`config.toml`](https://github.com/tyger-technology/tyger-minimal-blog/blob/master/exampleSite/config.toml). To use it, copy the [`config.toml`](https://github.com/tyger-technology/tyger-minimal-blog/blob/master/exampleSite/config.toml) in the root folder of your Hugo site. Feel free to change the strings in this theme.

You may need to delete the line: `themesDir = "../.."`

The example config file includes an menu for an about page and both post and project sections:

{{< highlight toml >}}
[[menu.main]]
identifier = "about"
name       = "About"
url        = "/about/"
weight     = 3

[[menu.main]]
identifier = "posts"
name       = "Posts"
url        = "/post/"
weight     = 1

[[menu.main]]
identifier = "projects"
name       = "Projects"
url        = "/project/"
{{< /highlight >}}

If want the menu to show only your sections, remove the example menu and add the following line to the config file:
{{< highlight toml >}}
sectionPagesMenu = "main"
{{< /highlight >}}

Refer to the Hugo docs for more information on [menu setup](https://gohugo.io/content-management/menus/).

The footer text, Twitter & Github links can be set in the config file:

{{< highlight toml >}}
[params]
  footerText = "Tyger Minimal Blog Theme"
  twitterUser = "GoHugoIO"
  githubUser = "gohugoio"
{{< /highlight >}}

## Theme Defaults

By default, the date is displayed for each content page. To hide the date for a page set:
`hide_date = true` in the frontmatter of that page.

The homepage is set to show list of posts in a *post* section. In the menu, the *post* item links to the homepage, while all other sections link to a list page showing their entries.

## Development

This theme includes the original SCSS files, which you can customize. Serveral NPM scripts are included to automate the compilation and minification of the SCSS files.

To install the development tools, run:

{{< highlight Bash >}}
$ npm install
{{< /highlight >}}

To launch the hugo server with the example site and watch for any changes to the SCSS files, run:
{{< highlight Bash >}}
$ npm run watch
{{< /highlight >}}

 To compile and minify the SCSS files to CSS in the `static` directory, run:
{{< highlight Bash >}}
$ npm run build
{{< /highlight >}}

## Contributing

Have you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](https://github.com/tyger-technology/tyger-minimal-blog/issues) to let me know.

## License

This theme is released under the [MIT license](https://github.com/tyger-technology/tyger-minimal-blog/blob/master/LICENSE.md).
