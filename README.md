# Quarto templates for UKCEH

This repository is intended to provide templates for Quarto documents, with a consistent UKCEH-specific theme across each [output format](#output-formats).

> [!IMPORTANT]
> This is a work in progress and all templates should be considered _unofficial_.


## Types of template/extension (planned and implemented)

- [ ] Basic document template (html, pdf)
- [ ] Presentation (revealjs) mirroring official UKCEH powerpoint template
- [ ] Report (html, pdf, docx) mirroring offical UKCEH report template
- [ ] Manuscript (project template)
- [ ] Book (project template)
- [ ] Website (project template, including dashboard?)


## Basic usage

### Getting _brand.yml

You will also need a local copy of the `_brand.yml` configuration file, which is hosted over at [github.com/ukceh-rse/brand-yml](https://github.com/ukceh-rse/brand-yml).
This file defines colours, typography, logos and layouts for maintaining consistent branding across formats.

For now, the easiest way to proceed is to symlink `_brand.yml` and the `logos/` directory into the project directory. This should improve in the future - see [this issue](https://github.com/ukceh-rse/quarto-templates/issues/1).


### Starting from scratch

To create a new document or project using a template, run

```sh
quarto use template ukceh-rse/quarto-templates/<subdir>
```

where `<subdir>` is the name of the subdirectory of this repository containing an extension and template, or template only.

To render the document or project to a specific format (e.g. `html`, `pdf`), run

```sh
quarto render <document>.qmd --to <extended-format>
```

where `<extended-format>` is structured as `<extension>-<format>`.

For example, if you use the `basic` extension & template, which implements `basic-html` and `basic-pdf`, to create a document called `test-doc.qmd`, you can render to html using

```sh
quarto render test-doc.qmd --to basic-html
```

You can omit the `--to <extended-format>` if you want to render to all available formats (in this case html and pdf), or if there is only one format implemented (e.g. for a presentation).


### Starting from an existing document or project

If you already have a document or project and you only want to download the extension _without_ the template, you can run

```sh
quarto add ukceh-rse/quarto-templates/<subdir>
```

and then manually change the format to an implemented `<extended-format>` in your `.qmd` file(s).


### Updating the extension

If the extension has changed upstream, you can run

```sh
quarto update ... #TODO
```


## Inspiration

- https://github.com/quarto-journals
- https://github.com/quarto-ext/typst-templates
- https://github.com/coatless-quarto/stanford/

