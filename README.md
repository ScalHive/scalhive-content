# scalhive-content

The intent of this repository is to develop the content of the scalhive organization's website using the Hugo framework.

## Useful links:

- [Hugo documentation](https://gohugo.io/documentation)
- [Hugo Installation](https://gohugo.io/installation/)
- Theme - [scalhive-content](https://github.com/TNTU-RS-internship/scalhive-theme.git)
- [Hugo docker images](https://hub.docker.com/r/klakegg/hugo)
- [Hugo Internal Templates](https://github.com/gohugoio/hugo/tree/master/tpl/tplimpl/embedded/templates)
- [Hugo themes](https://themes.gohugo.io/)
- [Tachyons documentation](http://tachyons.io/docs/)
- [Tachyons color codes](https://tachyons.io/docs/themes/skins/) for base theme
- Blogpost - [Image processing using hugo](https://clavinjune.dev/en/blogs/image-processing-using-hugo/)
- Blogpost - [Multilingual](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-1-managing-content-translation/)
- [Go text template](https://pkg.go.dev/text/template)
- Article [Add Contact form to Hugo with Google forms](https://blog.puvvadi.me/posts/add-contact-form-hugo-google-forms/)
- [Add-ons for Hugo](https://hugocodex.org/add-ons/) - Extend Hugo’s functionality

## [Hugo Installation](https://gohugo.io/installation/)

### Prerequisites

- [Git](https://git-scm.com/)
- [Go](https://go.dev/)
- [Dart Sass](https://gohugo.io/hugo-pipes/transpile-sass-to-css/#dart-sass)

Git is required to:

- Build Hugo from source 
- Use the Hugo Modules feature 
- Install a theme as a Git submodule 
- Access commit information from a local Git repository 
- Host your site with services such as CloudCannon, Cloudflare Pages, GitHub Pages, GitLab Pages, and Netlify

Go is required to:

- Build Hugo from source
- Use the Hugo Modules feature

Dart Sass is required to transpile Sass to CSS when using the latest features of the Sass language.

#### Check if the tools are installed

```shell
git version
go verison
```

If you'll install Hugo as a [Snap package](https://gohugo.io/installation/linux/#snap) - there is no need to install Dart Sass. The Hugo Snap package includes Dart Sass.

Installation instructions:
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Go](https://go.dev/doc/install)
- [Dart Sass](https://gohugo.io/hugo-pipes/transpile-sass-to-css/#dart-sass)

### [Hugo Linux Installation](https://gohugo.io/installation/linux/)

Snap:
```shell
sudo snap install hugo
```

Homebrew:
```shell
brew install hugo
```

Check if Hugo are installed correctly:
```shell
hugo version
```

## Deploy
Website is deploying automatically using GitHub Pages technology from 2 branches - `main` and `dev`

For local deploy use command:
```shell
docker-compose up
```
The site will be available at http://localhost:1313.

## Multilingual

Each markdown file that represent separate site page must have appropriation in each site language, otherwise language
button won't be presented in Menu. If some page isn't translated to other language, please for empty markdown files use
below text as page content.

For English
```text
Unfortunately, the page is not translated into this language.
```

For Ukrainian
```text
На жаль, сторінка не перекладена на цю мову.
```

## Images

could be stored in two places: `/static/` or `/assets/` folders.
- use `/assets/` folder for images which will be presented in page `main` section (images will be rendered by build);
- use `/static/` folder for background images specified in CSS code `{ background: url(""); }` (banner and header images) and for images which will be used for sharing but not presented on the site anywhere (such images won't be rendered by build).
