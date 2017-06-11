  [![Deploy to now](https://deploy.now.sh/static/button.svg)](https://deploy.now.sh/?repo=https://github.com/infiniteluke/blog)

# Next Static Blog
A simple static blog powered by [next.js](https://github.com/zeit/next.js)

## Usage
* `yarn`
* `yarn run export`
* `cd out`
* `now`

### Adding a Post
* Create a `.js` file in `posts`.
* Export an object that contains post content/metadata
```js
module.exports =  {
  title: 'Title',
  slug: 'slug',
  author: 'Your Name',
  date: new Date(),
  tags: [
    'tags',
    'go here'
  ],
  body: `
  ## Post
  Use markdown to _write_ your post
  Here's some code:
  \`\`\`
  const a = 'thing';
  \`\`\`
  `
};
```
* Inside `./posts/index.js` require your new post and add it to the exported array.
* Re-run `yarn run export` to build your new site.
