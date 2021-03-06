# Contributing

Contributions to this repository are welcome.

I appreciate feedback of any kind via [GitHub issues](https://github.com/danburzo/percollate/issues):

-   bug reports
-   feature suggestions
-   examples of web pages where `percollate` could do a better job

You can contribute to the code via [pull requests](https://github.com/danburzo/percollate/pulls). For small, straightforward fixes, you can create a PR directly. For more sophisticated changes, please open an issue beforehand to make sure we're on the same page.

## Common tasks

## Set up the project locally

Clone the repository to your local computer:

```bash
git clone git@github.com:danburzo/percollate.git
cd percollate
```

Then install the necessary dependencies:

```bash
npm install
```

You can then run the CLI by using `./cli.js` instead of `percollate`:

```bash
./cli.js pdf --output some.pdf http://example.com
```

> 💡 You may need to add _execution permissions_ to the file using `chmod +x ./cli.js`

## Check that an EPUB is valid

We use the excellent [epubcheck](https://github.com/w3c/epubcheck) Java tool to validate EPUBs generated by percollate.

```bash
npx epubcheck ./book.epub
```

## Debug the temporary HTML

If the generated PDF doesn't look like you'd expect, use the `--debug` flag  to save to the disk the temporary HTML file that `percollate` generates. Open the HTML in your browser to inspect the markup and styles.

## Run the code checks

Code is formatted automatically by [Prettier](https://prettier.io) on each commit. Additionally:

* `npm run lint` runs eslint on the codebase to enforce more aspects of coding style;
* `npm run test` runs the automated tests to ensure things work as expected.