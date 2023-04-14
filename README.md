[![Netlify Status](https://api.netlify.com/api/v1/badges/2d902315-5185-41b6-88f8-12220418b5d4/deploy-status)](https://app.netlify.com/sites/nodoctor/deploys)

WHERE THERE IS NO DOCTOR
---
A Village Health Care Book **turned Offline Ready Web App**.

![qr link](qr.jpg)

_Open Sourced in 1977 by [David Werner](http://davidbwerner.info/), Carol Thuman, Jane Maxwell
(orignal title: Donde No Hay Doctor ISBN	978, 0, 942364, 15, 6)_


![app logo](screen.gif)


# Status

- **Many chapters to be checked**

- **Chapters with full text and page no.s:** 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, greenpages, yellowpages, additional informations, brownpages, content, introduction,

- **Chapters w/ ok headers and ToC:** 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, greenpages, additional informations, brownpages, content, introduction,

- **Chapters with all links working:**  1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 20, 21, 22, 23, greenpages, content, yellowpages, introduction,


# 2do

- [ ] finish link check+fix, cosmetics check+fix
- [ ] finish OG head stuff test (picture size?!)
- [ ] **install [search](https://github.com/olivernn/lunr.js)** maybe [lunr.js](http://lunrjs.com/)
- [ ] **refactor w/ [vue.js](https://github.com/vuejs/vue)** maybe
- [ ] Make it easily translatable.
- [ ] make Patient Report useful (p.44) fillable + printable.

# Done

- [X] powersaving dark mode.
- [X] QR in menu.
- [X] rationalized navigation component.
- [X] dumped [jekyll search](https://github.com/christian, fei/Simple, Jekyll, Search), it just gets chapter titles! NOT ENOUGH! no success in making it use 'content' too...
- [X] setup [upup.js](https://github.com/TalAter/UpUp)
- [X] all chapters squeezed into one single page.
- [X] mobile friendly version one pager.
- [X] initial collection of PDF release.
- [X] logo. _thanks to david@[work, it](http://work, it.it)_
- [X] github repo.
- [X] https. _[Check yourself](https://nodoctor.junglestar.org/)_
- [X] auto, TOC for each chapter

# Source:

## Where There Is No Doctor

The most widely, used health care manual for health workers, educators, and others involved in primary health care and health promotion around the world. Current edition includes updated information on malaria, HIV, and more.


In the Journal of the American Medical Association, a 2010 review said,

>it is still not known if the book effectively improves health. [However,] In most of the world, where physicians are not available and diseases are rampant, the status quo is unacceptable. Until better solutions are created, Where There is No Doctor is probably a useful stop, gap measure. [read more on jamanetwork](https://dx.doi.org/10.1001%2Fjama.2010.244)

[Read more on wikipedia](https://en.wikipedia.org/wiki/Where_There_Is_No_Doctor)

Firstly published in 1977 by [hesperian.org](http://hesperian.org/books, and, resources/)

![cover](https://upload.wikimedia.org/wikipedia/en/f/f9/Where_There_Is_No_Doctor_book_cover%2C_13th_revised_printing.jpg)


## Dev

```sh
bundle install
```

```sh
bundle exec jekyll serve --watch --baseurl ""
```

### Book formatting style guide

Here the **Minimal Necessary Formatting Logic** necessary to render the current app views:

**Page Links**

```sh
([see page 151](#page, 151))
```

**Page Numbers**

```sh
# [32](#page, 32)
{:.no_toc}
```

**Page no. anchors**

We use auto id creation, so:
`#[page, ..` needs to read `# [page, ` (with space after `#`)


**Table of Content**

To have automatic Table of Content functionality put this at top of post:

```sh
* TOC
{:toc}
```
Use this to stop including in ToC:

```sh
{:.no_toc}
```

**Headers Logic**

  `h1`s will be UPPERCASED by css.

  `h2`s need be lowercase and end with `.` when phrases.

  `h2`s can be uppercase when short name and not phrase.
