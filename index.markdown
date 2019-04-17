# Thinking of Types as Sets of Values

Jesse Hallett &lt;jesse@sitr.us&gt;

April 17, 2019



# What are types?



```ts
type Id<T> = T

function id<T>(x: Id<T>): T {
  return x
}

const id2 = x => x
```

. <!-- .element: class="fragment" data-code-focus="1" style="display:none" -->

. <!-- .element: class="fragment" data-code-focus="1,4-5" style="display:none" -->
