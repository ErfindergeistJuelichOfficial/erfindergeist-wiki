> [!NOTE]
> Die Wiki ist umgezogen, der öffentliche Link lautet: [wiki.erfindergeist.org](wiki.erfindergeist.org)
> 
> Mitglieder können diese unter folgendem Link editieren: [docs.erfindergeist.org](docs.erfindergeist.org)

# Erfindergeist Wiki

The wiki is rendered to a static page using [hugo](https://gohugo.io/). It is deployed to Github pages and hosted at:\
**https://wiki.erfindergeist.org/**

## Installation

Install `hugo` and `go` using your favorite package manager (https://gohugo.io/installation/).

## Usage

Start a server (`-D` to build drafts as well). The server will automatically recompile and reload the pages in your browser.
```
hugo server -D
```
Navigate to `http://localhost:1313/` in your browser to view the page.

To create a new page, run
```
hugo new docs/werkstatt/geraete/schneideplotter.md
```
The page will be located under `content/`.
To mark the page as a draft which is not be rendered on the final page add `draft: true` to the page's frontmatter.

After merging or pushing to the `main` branch, a pipeline runs which compiles the static content and pushes it to Github pages.
