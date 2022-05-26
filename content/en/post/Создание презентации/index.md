---
title: Создание презенетаций в Mardown
subtitle: Презентация из кода! 

# Summary for listings and search engines
summary: Инструкция для презентаций

# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  - 吳恩達

tags:
  - Academic
  - 开源

categories:
  - Demo
  - 教程
---

## Overview

1. Окно редактора имеет подсветку синтаксиса «Маркдаун» и обеспечивает самые базовые операции с текстом как вставка, копирование и другое.

Окно просмотра презентации может работать в трёх режимах. Переключаться между режимами можно по кнопкам в правом нижнем углу этого окна. Или через главное меню «View».

По умолчанию в программе открывается режим просмотра отдельного слайда (см. Фиг. 1 выше). Навигация по слайдам в этом окне оригинальная:. Чтобы перейти на нужный слайд, нужно кликнуть манипулятором мышь в окне редактора на текст этого слайда.

Есть режим просмотра преобразованного текста «Маркдаун» в HTML, как в браузере.

Теперь об особенностях форматирования презентаций. Marp разбивает текст «Маркдаун» на слайды с помощью набора символов --- из трёх дефисов, которые в разметке текста «Маркдаун» используются для обозначения горизонтальной линии.

Слайд 1
Содержание слайда…

---

Слайд 2
Содержание слайда…

При этом сама горизонтальная линия в Marp отображаться не будет. 

2. Marp даёт возможность применять разные параметры и эффекты к презентации и отдельным слайдам Это делается с помощью специальных директив, которые нужно заключить в комментарии HTML <!-- -->

<!--
Имя директивы 1:  значение 
Имя директивы 2 : значениеe
…
Имя директивы N : значениеe
-->

Директива page_number

Это директива управляет отображением номеров страниц в презентации. Зачения: true, false.

<!--
page_number: true
-->

Директива $theme

Это директива позволяет выбрать визуальную тему для презентации. На текущий момент в программе две темы: default и gaia.

<!-- $theme: gaia -->

В дальнейшем, наверное, этих тем будет больше.
Директива template

Визуальная тема может имеет разные варианты — тёмная светлая. Для выбора не по умолчанию варианта темы имеется директива template со значением invert.

<!--
$theme: gaia
template: invert
-->

Директивы $width, $height

Директивы $width, $height задают физический размер слайдов. Значения

    px (по умолчанию), cm, mm, in, pt, pc.

Директива $size

Директива $size задаёт пропорции и ориентацию слайдов презентации. Параметры: 4:3, 16:9, A0-A8, B0-B8. Суффикс -portrait задаст портретную ориентацию слайдам.

<!-- $size: 16:9 -->

Глобальные и локальные директивы

Директивы $width, $height, $size, $theme являются глобальными и действуют на все слайды презентации. Директивы template, page_number могут действовать локально только, если их вставить в отдельный слайд. Для этого директива должна иметь в начале символ *.

<!-- *page_number: false -->
<!-- *template: invert -->

3. 

Нужно отметить, что подход к использованию «Маркдаун» может вызвать вопросы о нарушении главных простых принципов этой размётки текста «не загромождай» и «без обязательной латиницы».

Директивы Marp могут выглядеть как попытка нагромоздить в «Маркдаун» излишние сущности и навязать обязательное использование латиницы». Для мышления программистов характерно воспринимать любой текстовой файл как код условной программы. А размётка «Маркдаун» — всё же таки текст, а не код.

С другой стороны в пределах одной программы эти директивы вполне допустимы. Главное, чтобы в последующих версиях приложения не было погони за большим количеством директив.
{{< figure src="https://raw.githubusercontent.com/wowchemy/wowchemy-hugo-modules/master/academic.png" title="The template is mobile first with a responsive design to ensure that your site looks stunning on every device." >}}

## Get Started

- 👉 [**Create a new site**](https://wowchemy.com/templates/)
- 📚 [**Personalize your site**](https://wowchemy.com/docs/)
- 💬 [Chat with the **Wowchemy community**](https://discord.gg/z8wNYzb) or [**Hugo community**](https://discourse.gohugo.io)
- 🐦 Twitter: [@wowchemy](https://twitter.com/wowchemy) [@GeorgeCushen](https://twitter.com/GeorgeCushen) [#MadeWithWowchemy](https://twitter.com/search?q=%23MadeWithWowchemy&src=typed_query)
- 💡 [Request a **feature** or report a **bug** for _Wowchemy_](https://github.com/wowchemy/wowchemy-hugo-modules/issues)
- ⬆️ **Updating Wowchemy?** View the [Update Tutorial](https://wowchemy.com/docs/hugo-tutorials/update/) and [Release Notes](https://wowchemy.com/updates/)

## Crowd-funded open-source software

To help us develop this template and software sustainably under the MIT license, we ask all individuals and businesses that use it to help support its ongoing maintenance and development via sponsorship.

### [❤️ Click here to become a sponsor and help support Wowchemy's future ❤️](https://wowchemy.com/plans/)

As a token of appreciation for sponsoring, you can **unlock [these](https://wowchemy.com/plans/) awesome rewards and extra features 🦄✨**

## Ecosystem

- **[Hugo Academic CLI](https://github.com/wowchemy/hugo-academic-cli):** Automatically import publications from BibTeX

## Inspiration

[Check out the latest **demo**](https://academic-demo.netlify.com/) of what you'll get in less than 10 minutes, or [view the **showcase**](https://wowchemy.com/user-stories/) of personal, project, and business sites.

## Features

- **Page builder** - Create _anything_ with [**widgets**](https://wowchemy.com/docs/page-builder/) and [**elements**](https://wowchemy.com/docs/content/writing-markdown-latex/)
- **Edit any type of content** - Blog posts, publications, talks, slides, projects, and more!
- **Create content** in [**Markdown**](https://wowchemy.com/docs/content/writing-markdown-latex/), [**Jupyter**](https://wowchemy.com/docs/import/jupyter/), or [**RStudio**](https://wowchemy.com/docs/install-locally/)
- **Plugin System** - Fully customizable [**color** and **font themes**](https://wowchemy.com/docs/customization/)
- **Display Code and Math** - Code highlighting and [LaTeX math](https://en.wikibooks.org/wiki/LaTeX/Mathematics) supported
- **Integrations** - [Google Analytics](https://analytics.google.com), [Disqus commenting](https://disqus.com), Maps, Contact Forms, and more!
- **Beautiful Site** - Simple and refreshing one page design
- **Industry-Leading SEO** - Help get your website found on search engines and social media
- **Media Galleries** - Display your images and videos with captions in a customizable gallery
- **Mobile Friendly** - Look amazing on every screen with a mobile friendly version of your site
- **Multi-language** - 34+ language packs including English, 中文, and Português
- **Multi-user** - Each author gets their own profile page
- **Privacy Pack** - Assists with GDPR
- **Stand Out** - Bring your site to life with animation, parallax backgrounds, and scroll effects
- **One-Click Deployment** - No servers. No databases. Only files.

## Themes

Wowchemy and its templates come with **automatic day (light) and night (dark) mode** built-in. Alternatively, visitors can choose their preferred mode - click the moon icon in the top right of the [Demo](https://academic-demo.netlify.com/) to see it in action! Day/night mode can also be disabled by the site admin in `params.toml`.

[Choose a stunning **theme** and **font**](https://wowchemy.com/docs/customization) for your site. Themes are fully customizable.

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/wowchemy/wowchemy-hugo-modules/blob/master/LICENSE.md) license.
