# Demo for Dart Sass on Hugo

This is a minimal [Hugo](https://gohugo.io) project which demonstrates the use of the [standard Sass package](https://github.com/sass/sass) with Hugo for compatibility with [Dart Sass](https://sass-lang.com/dart-sass), rather than the [deprecated LibSass implementation](https://sass-lang.com/blog/libsass-is-deprecated) which is built into Hugo.

For more information, see https://www.brycewray.com/posts/2022/03/using-dart-sass-hugo/.

## Instructions

1. If you haven’t already done so, [install `npm`](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).

2. Clone this repository.

3. Run `npm run start` to launch the Hugo development server (at http://localhost:1313) with Dart Sass running. If you wish, you then can:
- Edit the `content/_index.md` and `content/test.md` files to confirm that Hugo live-updates their content.
- Edit the `assets/scss/_global.scss` and `assets/scss/index.scss` files to confirm that Sass is live-updating the styling.

4. The build command is `npm run build`.

**Note**: Of course, using the regular `hugo server` (development) and `hugo` (production) commands will bypass the `package.json` scripting, thus not running Dart Sass. Further, this will cause remote build attempts to crash because [Hugo Pipes](https://gohugo.io/hugo-pipes) won’t get a Sass-generated `assets/css/index.css` file to process.