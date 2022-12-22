# Chart Hill Demo

Demo for [Chart Hill](https://github.com/travishorn/chart-hill), a chart
component library for Vue 3.

## Installation

The library is not published on npm, yet. Until then, you can manually install
the library and this demo.

Clone this repository

```sh
git clone https://github.com/travishorn/chart-hill-demo
```

Clone the Chart Hill repository

```sh
git clone https://github.com/travishorn/chart-hill
```

Install dependencies for both projects

```sh
cd chart-hill-demo
npm install
cd ../chart-hill
npm install
```

Build the library and link it

```sh
npm run build
npm link
```

Finally, link the demo to the library

```
cd ../chart-hill-demo
npm link chart-hill
```

### Run development server

```sh
npm run dev
```

Visit the demo page in your web browser at the URL displayed in your terminal.

## License

The MIT License (MIT)

Copyright © 2022 Travis Horn

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the “Software”), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
