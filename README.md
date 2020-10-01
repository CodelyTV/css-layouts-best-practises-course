# 📐 CSS Layouts Best Practises

Code related to the [CSS Layouts Best Practises course](https://pro.codely.tv/library/layouts-css/)

## 🕵️ Project structure

Lesson related content is inside the `/pages` folder. For each lesson there is a `/components` folder, whre you can find each component's html and css together in a [single file component](https://vuejs.org/v2/guide/single-file-components.html).

In `/common` you will find the components that remain unchanged throughout the course.

If you prefer, you can also inspect the code for each lesson on the [demo page](https://codelytv.github.io/css-layouts-best-practises-course/) with your devtools, or run the project locally as seen in the next section.

## 🏗️ Build Setup

If you wish to run the project locally:

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# or generate static project and serve dist folder at localhost:3000
$ npm run generate
$ npm run start
```

Generated html files are in the `/dist` folder. CSS files are extracted to `/dist/_nuxt/pages`
