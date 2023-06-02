# Toolbox Font

This npm package contains the TenForce font (`src/fonts/tenforce.woff`) and the Source Sans Pro font (`src/fonts/SourceSansPro-*.ttf`).

## Usage
Both font packages can be imported using the `style.scss` file, but there are also separate SCSS files in case you only need one set of them:
- `src/styles/source-sans-pro.scss`
- `src/styles/tenforce-font.scss`

``` scss
@import "~@tenforce/toolbox-fontmap/dist-lib/styles/style";
```

## Symbols Utility
Starting v2.0.0 we have added the `src/utils/Symbols.ts` file, which maps every TenForce icon to a named variable, to make usage of the font more readable in our code.

``` js
import { Symbols } from "@tenforce/toolbox-fontmap"
```

## Updating the TenForce font
1. Update the `src/fonts/tenforce.woff` file.
    - Make sure the filename stays the same.
2. Adding new icons.
    - Add new icons to `src/utils/Symbols.ts`.
    - Add new tags to the demo page `example/src/utils/tags.ts`.
3. Removing icons.
    - Remove icons from `src/utils/Symbols.ts`.
    - Remove tags from `example/src/utils/tags.ts`.


## Demo page
The demo page will render every single icon in the TenForce font. It also supports search on tags, which are stored in `example/src/utils/tags.ts`.

Besides this, when you click on an icon, you will see:
- character code
- name
- unicode
- tags

### Running the demo application
To run the demo page, simply go to the `example` folder and:
``` bash
yarn install
yarn start
```
