# Test Case

Minimal test case for:

- https://github.com/gatsbyjs/gatsby/issues/30199
- https://github.com/andrewbranch/gatsby-remark-vscode/issues/144

## Reproduction

It seems the issue is happening when gatsby-remark-vscode & gatsby-source-graphql are combined with Gatsby v3.

```bash
git clone git@github.com:kremalicious/gatsby-test-case-30199.git
cd gatsby-test-case-30199
npm i

# before starting, make sure you have a `GITHUB_TOKEN` exported,
# or in an .env file
npm start
```

Now open markdown file `content/hello-world/index.md` and save the file one or multiple times. The console will output this error:

```bash
Missing onError handler for invocation 'building-schema', error was 'Error: Schema must contain
uniquely named types but contains multiple types named "GRVSCStylesheet".'. Stacktrace was 'Error:
 Schema must contain uniquely named types but contains multiple types named "GRVSCStylesheet".
```
