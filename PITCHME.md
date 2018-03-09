# Tips & Tricks
### replace the
```html
<!-- .element: class="fragment" -->
```
### with `|`

---

## Who am I?
# Pesho <!-- .element: class="fragment" -->
### More at the end <!-- .element: class="fragment" -->

---

# What's the talk about?
## DevTools <!-- .element: class="fragment" -->
## Techniques <!-- .element: class="fragment" -->
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

## have fun!
Note:
  - everything you see except the network tab should be possible (haven't tried)

+++

## [more info](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27)

---

## The good old breakpoint
### no demo :( <!-- .element: class="fragment" -->
Note:
  - if you came for it - sorry, we will mention it though :)
  - high risk, manu ppl could leave

+++

## The automatic breakpoint you need
#### (workflow demo) <!-- .element: class="fragment" -->

Note:
  - prettify if needed
  - climb up the stack and find your domain code
  - look around & think

+++

## Come again?
  - prettify
  - select to inspect
  - blackbox the scripts you want to ignore

+++

You have “fixed” the code and now it produces wrong results (awesome it does not blow but you have no idea wtf is going on). I present you the ‘debugger’ statement.
