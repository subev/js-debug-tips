# Tips & Tricks

---

## Who am I?
# Pesho <!-- .element: class="fragment" -->
### More at the end <!-- .element: class="fragment" -->

---

# What's the talk about?
- ## DevTools <!-- .element: class="fragment" -->
- ## Techniques <!-- .element: class="fragment" -->
# What Audience? <!-- .element: class="fragment" -->

Note:
  - "I was too busy fixing bugs to explore what tools are out there"
  - What if I use Mozilla, Internet Exploder? (hell ye I had to mention it)
  - everyone has his/her style, I will share you mine
  - my workflow for certain situtations (maybe there are better)

+++

# What the talk is not about?
## Replacing your IDE <!-- .element: class="fragment" -->
Note:
  - although there is such support, it is too much in the long run

+++

# NodeJS apps

### or not exactly! <!-- .element: class="fragment" -->

+++

## `node --inspect index.js`
### (v6.3.0+ required) <!-- .element: class="fragment" -->

+++

## `chrome://inspect`
![Logo](https://cdn-images-1.medium.com/max/1600/1*x4VXx50dLdD_HbqE6hpIRw.png)
#### [more info](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27) <!-- .element: class="fragment" -->

Note:
  - everything you see except the network tab should be possible (haven't tried)

+++

## Framework specific tools
### React / Vue / Angular Dev tools
Note:
  - ye they provide a lot, and it is strongly suggested to have them if you are developing and  you want to save time
  - on production they are set to be disabled
  - those techniques and tools are unique and framework agnostic!

---

## The good old breakpoint
### no demo :( <!-- .element: class="fragment" -->
Note:
  - if you came for it - sorry, we will mention it though :)
  - high risk, many ppl could leave
  - joke aside, we will see it probably thourghout the demos

+++

## [The automatic breakpoint and stack traversing](https://dojo.telerik.com/AKIWixIh/2)
#### Workflow demo
 - enable it
 - dive down the stack
 - look around & think

Note:
  - prettify if needed
  - climb up the stack and find your domain code
  - look around & think

+++

## "Sorry I wasn't watching, what was that?"
  - explore the stack (up and down)
  - prettify
  - select to inspect
  - blackbox the scripts you want to ignore

---
## Conditional breakpoint
### let's abuse it in a demo! <!-- .element: class="fragment" -->

+++

## "Repeat again, please!"
  ![Logo](https://data.whicdn.com/images/280941599/large.jpg) <!-- .element: class="fragment" -->

+++

## BREAK(point)
### doesn't have to be true
### to be perfect

+++

  - debugger;
  - trace what function is invoked on interaction (event listeners) <!-- .element: class="fragment" -->
  - console.count <!-- .element: class="fragment" -->
  - bookmarklets <!-- .element: class="fragment" -->
  - $0 <!-- .element: class="fragment" -->
  - how not to write tests <!-- .element: class="fragment" -->
  - expose internal variables <!-- .element: class="fragment" -->
  - use debugger to debug the debug tools <!-- .element: class="fragment" -->

---

### Debugger Demo

---

### Searching Demo

---

### Shortcuts

---

### Profiling [Demo](https://nodesource.com)

+++

### Demo using profiler to get insights [Demo](http://www.mediapool.bg/)

---

### Network tab [demo](https://www.crunchbase.com/search/people)

---

### Other tools worth mentioning

---

Questions?

