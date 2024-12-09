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
quarto use template ukceh-rse/quarto-templates/ceh-<format>
```

where `ceh-<format>` should be the name of one of the subdirectories in this repository.

E.g. to use the RevealJS template

```sh
quarto use template ukceh-rse/quarto-templates/ceh-reveal
```

Refer to [the documentation](https://quarto.org/docs/extensions/formats.html#distributing-formats) for further details.


## Relationship with `_brand.yml`

The [`_brand.yml` configuration file](https://github.com/ukceh-rse/brand-yml) defines colours, typography, logos and layouts for maintaining consistent branding across formats.

In principle, `_brand.yml` should allow us to single-source this information.
Then, templates would only need to define structural elements specific to their specific format.

However, `_brand.yml` is in the very early stages of being integrated in the Quarto ecosystem, so the documentation in sparse and not everything works 'out of the box' right now.

In particular, it is not yet clear to me how best to incorporate a `_brand.yml` held in a separate GitHub repository into these templates.
(Note that `_brand.yml` is more general than Quarto.)

## Contributing

To do. For now, just raise an issue or contact me (Joe).

## Inspiration

- https://github.com/quarto-journals
- https://github.com/quarto-ext/typst-templates
- https://github.com/coatless-quarto/stanford/

