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
![union of List and Seq](./list-union-seq.svg)

---

<!-- .slide: class="noborder" -->
![an intersection type that contains sized collections](./collection-intersect-size.svg)

---

<!-- .slide: class="noborder" data-transition="none" -->
![unit types in string, number, and boolean](./unit-types.svg)

--

<!-- .slide: class="noborder" data-transition="none" -->
![null and undefined are unit types](./all-unit-types.svg)

---

<!-- .slide: class="noborder" data-transition="none" -->
![empty intersection](./empty-intersection.svg)

--

<!-- .slide: class="noborder" data-transition="none" -->
![empty intersection is never](./empty-intersection-is-never.svg)

---

<!-- .slide: data-transition="none" -->
```ts
function matchBoolean(x: boolean): string {
  switch(x) {
    case true:
      return "got true"
    case false:
      return "got false"
    default:
      return "what did we get?"
  }
}
```

. <!-- .element: class="fragment" data-code-focus="8" style="display:none" -->

--

<!-- .slide: data-transition="none" -->
```ts
function matchBoolean(x: boolean): string {
  switch(x) {
    case true:
      return "got true"
    case false:
      return "got false"
    default:
      x.someProp // ✘ 'someProp' does not exist on type 'never'.
      return "what did we get?"
  }
}
```

. <!-- .element: class="fragment" data-code-focus="8" style="display:none" -->
