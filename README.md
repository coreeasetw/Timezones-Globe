# Timezones Globe

https://observablehq.com/@raphaelchalicarne/timezones-globe@397

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@5
npm install https://api.observablehq.com/d/da9a8167025bf58e@397.tgz?v=3
~~~

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "@raphaelchalicarne/timezones-globe";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~

## GitHub Pages

This repository includes a GitHub Actions workflow that deploys the static
files in this folder to GitHub Pages from the `main` or `work` branch. To
publish the site:

1. Push your changes to GitHub on one of the monitored branches.
2. Ensure GitHub Pages is enabled for the repository and set to use the
   "GitHub Actions" source.
3. The workflow will upload the contents of the repository root and publish
   them at the configured Pages URL.
