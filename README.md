# unified-projects
meta-repo for contributions to the unnifedjs community


## Projects:

- __vfile-create-effects__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed
- __vfile-handle-effects-fs__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data represents files to be written to the fs
- __vfile-handle-effects-http__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data is an http call needing to be requested.
- __vfile-handle-effects-socket__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the data is a message to drop on a socket/websocket/zeromq connection etc. [FUTURE]
- __vfile-handle-effects-DOM__
  - util that allows plugin authors to emit new data that models side effects that still needing to be processed - where the effect is a virtual-DOM tree needing to be applied at some tree location. [FUTURE]
- __vfile-subscriptions__
  - [FUTURE Project] vfile effects could then be used as inputs for other plugins and effects
- __vfile-handle-effects__
  - batteries inluded plugin that applies the default effect handlers for each of the various types of side effects
- __unist-utill-slice__
  - chops up a unist tree into non-overlapping slices based on designated separator nodes
- __unist-util-chunk__
  - process a unist tree into possibly overlapping slices based on designated start/stop nodes
- __remark-content-separation-flags__
  - apply the `unist-util-slice` to the md(x)ast for remark usage
- __rehype-content-separation-flags__
  - apply the `unist-util-slice` to the hast for rehype usage
- __remark-mermaid-plugin-inline__
  - process the mermaid code blocks in remark content
- __remark-configure-nudge-cmment__
  - add a node to the frontmatter or comment to the top of prose letting future MD readers know that the content requires a specific plugin composition so that the content can be rendered.
  
  
