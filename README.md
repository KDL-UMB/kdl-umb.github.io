# al-folio
A simple and clean Jekyll theme for academics.

al-folio is based on *folio theme. The original theme was published by Lia Bogoev and copyrighted under the MIT license.

## Getting started

For more about how to use Jekyll, check out [this tutorial](https://www.taniarascia.com/make-a-static-website-with-jekyll/).
Why Jekyll? Read [Andrej Karpathy's blog post](https://karpathy.github.io/2014/07/01/switching-to-jekyll/)!


### Installation

#### Local setup

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), first [fork](https://guides.github.com/activities/forking/) the theme from `github.com:alshedivat/al-folio` to `github.com:<your-username>/<your-repo-name>` and do the following:

```bash
$ git clone git@github.com:<your-username>/<your-repo-name>.git
$ cd <your-repo-name>
$ bundle install
$ bundle exec jekyll serve
```

Now, feel free to customize the theme however you like (don't forget to change the name!).
After you are done, **commit** your final changes.

#### Deployment

Deploying your website to [GitHub Pages](https://pages.github.com/) is the most popular option.
**al-folio** will automatically re-deploy your webpage each time you push new changes to your repository! :sparkles:

## Features

### Publications

Your publications page is generated automatically from your BibTex bibliography.
Simply edit `_bibliography/papers.bib`.
You can also add new `*.bib` files and customize the look of your publications however you like by editing `_pages/publications.md`.

<p align="center"><img src="https://raw.githubusercontent.com/alshedivat/al-folio/master/assets/img/publications-screenshot.png" width=800></p>

<details><summary><strong>Author annotation:</strong></summary>

In publications, the author entry for yourself is identified by string `scholar:last_name` and string array `scholar:first_name` in `_config.yml`:
```
scholar:
  last_name: Einstein
  first_name: [Albert, A.]
```
If the entry matches the last name and one form of the first names, it will be underlined.
Keep meta-information about your co-authors in `_data/coauthors.yml` and Jekyll will insert links to their webpages automatically.
The coauthor data format in `_data/coauthors.yml` is as follows,
```
"Adams":
  - firstname: ["Edwin", "E.", "E. P.", "Edwin Plimpton"]
    url: https://en.wikipedia.org/wiki/Edwin_Plimpton_Adams

"Podolsky":
  - firstname: ["Boris", "B.", "B. Y.", "Boris Yakovlevich"]
    url: https://en.wikipedia.org/wiki/Boris_Podolsky

"Rosen":
  - firstname: ["Nathan", "N."]
    url: https://en.wikipedia.org/wiki/Nathan_Rosen

"Bach":
  - firstname: ["Johann Sebastian", "J. S."]
    url: https://en.wikipedia.org/wiki/Johann_Sebastian_Bach

  - firstname: ["Carl Philipp Emanuel", "C. P. E."]
    url: https://en.wikipedia.org/wiki/Carl_Philipp_Emanuel_Bach
```
If the entry matches one of the combinations of the last names and the first names, it will be highlighted and linked to the url provided.

</details>


### Collections

This Jekyll theme implements `collections` to let you break up your work into categories.
The theme comes with two default collections: `news` and `projects`.
Items from the `news` collection are automatically displayed on the home page.
Items from the `projects` collection are displayed on a responsive grid on projects page.

<p align="center"><img src="https://raw.githubusercontent.com/alshedivat/al-folio/master/assets/img/projects-screenshot.png" width=700></p>

You can easily create your own collections, apps, short stories, courses, or whatever your creative work is.
To do this, edit the collections in the `_config.yml` file, create a corresponding folder, and create a landing page for your collection, similar to `_pages/projects.md`.


### Layouts

**al-folio** comes with stylish layouts for pages and blog posts.

#### The iconic style of Distill

The theme allows you to create blog posts in the [distill.pub](https://distill.pub/) style:

<p align="center"><a href="https://alshedivat.github.io/al-folio/blog/2018/distill/" target="_blank"><img src="https://raw.githubusercontent.com/alshedivat/al-folio/master/assets/img/distill-screenshot.png" width=700></a></p>

For more details on how to create distill-styled posts using `<d-*>` tags, please refer to [the example](https://alshedivat.github.io/al-folio/blog/2018/distill/).

#### Full support for math & code

**al-folio** supports fast math typesetting through [KaTeX](https://katex.org/) and code syntax highlighting using [GitHub style](https://github.com/jwarby/jekyll-pygments-themes):

<p align="center">
<a href="https://alshedivat.github.io/al-folio/blog/2015/math/" target="_blank"><img src="https://raw.githubusercontent.com/alshedivat/al-folio/master/assets/img/math-screenshot.png" width=400></a>
<a href="https://alshedivat.github.io/al-folio/blog/2015/code/" target="_blank"><img src="https://raw.githubusercontent.com/alshedivat/al-folio/master/assets/img/code-screenshot.png" width=400></a>
</p>

#### Photos

Photo formatting is made simple using [Bootstrap's grid system](https://getbootstrap.com/docs/4.4/layout/grid/).
Easily create beautiful grids within your blog posts and project pages:

<p align="center">
  <a href="https://alshedivat.github.io/al-folio/projects/1_project/">
    <img src="assets/img/photos-screenshot.png" width="75%">
  </a>
</p>


### Other features

#### Theming
Six beautiful theme colors have been selected to choose from.
The default is purple, but you can quickly change it by editing `$theme-color` variable in the `_sass/_themes.scss` file.
Other color variables are listed there as well.

#### Social media previews
**al-folio** supports preview images on social media.
To enable this functionality you will need to set `serve_og_meta` to `true` in your `_config.yml`.
Once you have done so, all your site's pages will include Open Graph data in the HTML head element.

You will then need to configure what image to display in your site's social media previews.
This can be configured on a per-page basis, by setting the `og_image` page variable.
If for an individual page this variable is not set, then the theme will fall back to a site-wide `og_image` variable, configurable in your `_config.yml`.
In both the page-specific and site-wide cases, the `og_image` variable needs to hold the URL for the image you wish to display in social media previews.

#### Atom (RSS-like) Feed
It generates an Atom (RSS-like) feed of your posts, useful for Atom and RSS readers.
The feed is reachable simply by typing after your homepage `/feed.xml`.
E.g. assuming your website mountpoint is the main folder, you can type `yourusername.github.io/feed.xml`

## Contributing

Contributions to al-folio are very welcome!
Before you get started, please take a look at [the guidelines](CONTRIBUTING.md).

If you would like to improve documentation, add your webpage to the list below, or fix a minor inconsistency or bug, please feel free to send a PR directly to `master`.
For more complex issues/bugs or feature requests, please open an issue using the appropriate template.


## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

Originally, **al-folio** was based on the [\*folio theme](https://github.com/bogoli/-folio) (published by [Lia Bogoev](http://liabogoev.com) and under the MIT license).
Since then, it got a full re-write of the styles and many additional cool features.
