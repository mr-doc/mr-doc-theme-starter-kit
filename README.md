# Mr. Doc Theme Starter Kit
A responsive starter kit for Mr. Doc themes. 

*This starter kit is based on [mrdoc-theme-cayman](https://github.com/iwatakeshi/doxx-theme-cayman).*


## Requirements

* Ruby
* [Ruby Sass](http://sass-lang.com/install)
* Gulp
* Bower

## Usage

Create a bower file using `bower init` and add the following dependencies using `bower i --save`:

* `prism` - for syntax highlighting
* `bootstrap-sass` - for labels and other components

Of course, you are not limited to using bootstrap or sass and are free to use whatever frontend framework you like.

## Build

```bash
# Build the theme for production
gulp build
```

## Develop

```bash
# Build and watch the theme for development
gulp
```

## Customizations

By default, a Sass version of [Bootstrap](http://getbootstrap.com/) 
and a [custom Sass file](https://github.com/iwatakeshi/doxx-theme-starter-kit/blob/master/scss/index.scss) is used for the starter kit. Also, the starter kit is using gulp as its build system and it should be easy enough to see and understand that gulp is doing most of the hard work including minification.

## Publish

Create a package with `mr-doc-theme` as the keyword and add the following dev dependencies:

```bash
npm i --save-dev gulp gulp-shell gulp-connect gulp-ruby-sass gulp-clipboard gulp-uglify gulp-uglifycss lodash
```


Once you have created the package, you are free to customize the template under `template/`.
You may also edit the gulp file if you add more dependencies through bower. 

Just make sure that your assets are placed under `assets/` and that you edit the template to add those assets.

As far as the asset's paths are concerned, the relative path is taken care for you by Mr. Doc. You will only need to add `target.relative.path` to the asset's path as shown below.

Example: 

```jade
script(src=target.relative.path + 'js/...')

link(rel='stylesheet', href=target.relative.path + 'css/...')
```

When all is set and done, take a screenshot of your theme, add it to your readme using [Google Drive to host your image](https://www.thegooru.com/how-to-host-an-image-from-google-drive/), and publish the theme!

## License

This project is licensed under [Creative Commons Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/).
