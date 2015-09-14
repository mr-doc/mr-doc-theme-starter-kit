# Doxx Theme Starter Kit
A responsive starter kit for Doxx themes. 

*This starter kit is based on [doxx-theme-cayman](https://github.com/iwatakeshi/doxx-theme-cayman).*


## Requirements

* Ruby
* [Ruby Sass](http://sass-lang.com/install)
* Gulp
* Bower

## Usage

Create a bower file using `bower init` and prefix the name of your theme with
`doxx-theme-` and add `doxx` as your keyword. Then add the following dependencies using `bower i --save`:

* `prism` - for syntax highlighting
* `bootstrap-sass` - for labels and other components

Of course, you are not limited to using bootstrap or sass and are free to use whatever language you like.

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

By default a Sass version of [Bootstrap](http://getbootstrap.com/) 
and a [custom Sass file](https://github.com/iwatakeshi/doxx-theme-starter-kit/blob/master/scss/index.scss) is used for the starter kit. Also, the starter kit is using gulp as its build system and it should be easy enough to see and understand that gulp is doing most of the hard work including minification.

## Publish

Once the bower file has been created, you are free to customize the template under `template/`.
You may also edit the gulp file if you add more dependencies through bower. 

Just make sure that your assets are placed under `assets/` and that you edit the template to add those assets.

As far as asset's paths are concerned, the relative path is taken care for you by Doxx. You will only need to add
`target.relative.path` to the asset's path as shown below.

Example: 

```jade
script(src=target.relative.path + 'js/...')

link(rel='stylesheet', href=target.relative.path + 'css/...')
```

When all is set and done, you may publish the theme and use it with Doxx!

## License

This project is licensed under [Creative Commons Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/).