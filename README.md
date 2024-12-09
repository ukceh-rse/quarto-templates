# Quarto templates for UKCEH

This repository is intended to provide templates for Quarto documents, with a consistent UKCEH-specific theme across each [output format](#output-formats).

> [!IMPORTANT]
> This is a work in progress and all templates should be considered _unofficial_.


## Output formats

- [ ] HTML
- [ ] DOCX
- [ ] PDF
- [ ] RevealJS (see also https://github.com/ukceh-rse/quarto-reveal-template)
- [ ] Typst (pdf document, poster, ...)

## Usage

To create a new project using a template, run

```sh
quarto use template ukceh-rse/quarto-templates/<format>
```

where `<format>` should be the name of one of the subdirectories in this repository.

E.g. to use the RevealJS template

```sh
quarto use template ukceh-rse/quarto-templates/revealjs
```

## Working with _brand.yml

You also need a local copy of the `_brand.yml` configuration file, which is hosted over at [github.com/ukceh-rse/brand-yml](https://github.com/ukceh-rse/brand-yml).
This file defines colours, typography, logos and layouts for maintaining consistent branding across formats.

For now, the easiest way to proceed is to symlink `_brand.yml` and the `logos/` directory into the project directory. This should improve in the future - see [this issue](https://github.com/ukceh-rse/quarto-templates/issues/1).


## Inspiration

- https://github.com/quarto-journals
- https://github.com/quarto-ext/typst-templates
- https://github.com/coatless-quarto/stanford/

