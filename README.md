# CSS Layouts Best Practises Course

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# generate static project
$ npm run generate
```

Generated html files are in the `/dist` folder. CSS files are extracted to `/dist/_nuxt/pages`

## Project structure

Lesson related content is inside the `/pages` folder. For each lesson there is a `/components` folder, whre you can find each component's html and css together in a [single file component](https://vuejs.org/v2/guide/single-file-components.html).

In `/common` you will find the components that remain unchanged throughout the course.
