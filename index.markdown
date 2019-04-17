# Thinking of Types as Sets of Values

Jesse Hallett &lt;jesse@sitr.us&gt;

April 17, 2019

---

<!-- .slide: class="noborder" -->
![a portion of the interface hierarchy in Immutable.js](./interface-hierarchy.svg)

---

<!-- .slide: class="noborder" -->
![Immutable.js interfaces represented as nested sets](./interface-hierarchy-as-sets.svg)

---

<!-- .slide: class="noborder" data-transition="none" -->
![List and Seq, a pair of disjoint types](./list-and-seq.svg)

--

<!-- .slide: class="noborder" data-transition="none" -->
![List and Seq, a pair of disjoint types](./list-union-seq.svg)

---


```ts
type Id<T> = T

function id<T>(x: Id<T>): T {
  return x
}

const id2 = x => x
```

. <!-- .element: class="fragment" data-code-focus="1" style="display:none" -->

. <!-- .element: class="fragment" data-code-focus="1,4-5" style="display:none" -->
