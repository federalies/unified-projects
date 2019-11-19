# unified-projects
meta-repo for contributions to the unnifedjs community

## Projects:

### Remark plugins

- __[remark-content-separation-flags](https://github.com/federalies/remark-content-separation-flags)__
  - apply the `unist-util-slice` to the md(x)ast for remark usage
- __[remark-mermaid-plugin-inline](https://github.com/federalies/remark-mermaid-plugin-inline)__
  - process the mermaid code blocks in remark content
- __[remark-configure-nudge-cmment](https://github.com/federalies/remark-configure-nudge-cmment)__
  - add a node to the frontmatter or comment to the top of prose letting future MD readers know that the content requires a specific plugin composition so that the content can be rendered.

### Rehype plugins

- __[rehype-content-separation-flags](https://github.com/federalies/rehype-content-separation-flags)__
  - apply the `unist-util-slice` to the hast for rehype usage

### Unist-utils

- __[unist-utill-slice](https://github.com/federalies/unist-utill-slice)__
  - chops up a unist node/tree into non-overlapping slices based on designated separator nodes
- __[unist-util-chunk](https://github.com/federalies/unist-util-chunk)__
  - process a unist node/tree into possibly overlapping segments based on designated start/stop nodes

### Utils for Plugin Developers

- __[vfile-create-effects](https://github.com/federalies/vfile-create-effects)__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed
- __[vfile-handle-effects](https://github.com/federalies/vfile-handle-effects)__
  - a batteries inluded plugin that installs and uses all the following default `vfile-handle-effects-*` functions.
- __[vfile-handle-effects-fs](https://github.com/federalies/vfile-handle-effects-fs)__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data represents files to be written to the fs.
- __[vfile-handle-effects-http](https://github.com/federalies/vfile-handle-effects-http)__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data is an http call needing to be requested.
- __[vfile-handle-effects-socket](https://github.com/federalies/vfile-handle-effects-socket)__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data is a message to drop on a socket/websocket/zeromq connection etc. [FUTURE]
- __[vfile-handle-effects-dom](https://github.com/federalies/vfile-handle-effects-dom)__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the effect is a virtual-DOM tree needing to be applied at some tree location. [FUTURE]
- __[vfile-subscriptions](https://github.com/federalies/vfile-subscriptions)__
  - [FUTURE Project] vfile effects could then be used as inputs for other plugins and effects

### Templast Ecosystem (All work in progress)

- __[templast](https://github.com/federalies/templast)__

#### Handlebars Support
- __[templast-hbs-parse](#)__
  parse handlebars templates
- __[templast-hbs-verify](#)__
  parse handlebars templates // TASTY --> HBS dialect
- __[templast-hbs-stringify](#)__
  parse handlebars templates  --> HBS Dialect --> string

#### mustache Support
- __[templast-mustache-parse](#)__
- __[templast-mustache-verify](#)__
  assigns `warnings` or `failures` to the template if the source file was from some other template system and is now going to be rendered as a mustache file.
- __[templast-mustache-stringify](#)__

### doT Support
- __[templast-doT-parse](#)__
  incorporate doT templates into `templast`
- __[templast-doT-verify](#)__
  incorporate doT templates into `templast`
- __[templast-doT-stringify](#)__
  incorporate doT templates into `templast`

#### apacheVTL Support
- __[templast-apacheVTL-parse](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-apacheVTL-verify](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-apacheVTL-stringify](#)__
  incorporate apacheVTL templates into `templast`

### js Tempalte Literals
- __[templast-jsTemplateLiterals-parse](#)__
  incorporate jsTemplateLiterals into `templast`
- __[templast-verify-jsTemplateLiterals](#)__
  incorporate jsTemplateLiterals into `templast`
- __[templast-jsTemplateLiterals-stringify](#)__
  incorporate jsTemplateLiterals into `templast`

#### EJS Support
- __[templast-ejs-parse](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-verify](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-stringify](#)__
  incorporate apacheVTL templates into `templast`

#### EJS Support
- __[templast-ejs-parse](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-verify](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-stringify](#)__
  incorporate apacheVTL templates into `templast`


#### JADE Support
- __[templast-ejs-parse](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-verify](#)__
  incorporate apacheVTL templates into `templast`
- __[templast-ejs-stringify](#)__
  incorporate apacheVTL templates into `templast`



## Roadmap

- type-system guarentees
- help needed for `jade`
- help needed for `pug`
- subset of `EJS`
- subset of `ERB`
- explore supporting some subset of "PHP templates"

### Usage

`npm start` will download a ton of other git repos into the packages folder. 
Where each of the packages have their own repo and lifecycle.

Then use the `npx meta` command to manage all those sub-repos in some type of `lerna-overlord-style`

### PIPEDREAMS

- to-and-fro-Apache-Velocity-Templates
  - Parse VTL to unist
  - Parse mustache to unist
  - Parse mustache to unist
  - VTL to mustache ?? https://mustache.github.io/mustache.5.html?
    + hash lookups
    + hash context windows - and subsequent attribute lookups
    + comments
    + partials
  - VTL to handlebars
    + hash lookups
    + hash context windows - and subsequent attribute lookups
    + HTML escaping
    + block expressions
    + consider it a foreach
        + Sets context to a list and allows attributes to be read for each item
    + nested attr.path
    + context stack can be traversed upward
    + comments
    + helpers can be registered
        + built in `#with` and `#each`
    + partials
  - TemplateAST
    - Mustache
    - Handlebars
    - Apache VTL
    - JS Template Strings
    - doT
    - EJS
    - Pug
    - Marko?
    - Jade
  - VTL to MDX?
  - mustache to VTL
  - handlebars to VTL

- Babel7Ast-to-mdxast

  - ref: https://github.com/babel/babel/blob/master/packages/babel-parser/ast/spec.md

- TSast-to-mdxast

- MDXAST

    - MDAST + 

    - JSX -> script

    - COMMENT

    - Import

    - Export

- MDXHAST

    - HAST +
        type: element
        tagName: div, span, form, input, 
        properties: {}
        children:[]
        ƒ h(tagType, {props}, [ children ] )

    - imports

    - exports

    - inlineCode

means that an .mdx file is really a fancy JS file 
a certain type of JS file that has some convention allowing it to be rendered when invoked with proper context 

