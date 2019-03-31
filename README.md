# docker-hugo

A hugo container with asciidoctor extensions.

## Usage

Simply consuming this container as the hugo container is consumed should work fine.

### Caveats

This container comes with an opinionated set of asciidoctor extensions. 
[There is no way to customize asciidoctor library invocation](https://discourse.gohugo.io/t/customize-asciidoctor-parameters/14440)
so the container automatically loads certain libraries automatically.

This means there additional requirements for any project that uses both asciidoctor and this container. These
include:

- A (possibly empty) `bibliography.bib` file in the project root (for asciidoctor-bibtex)