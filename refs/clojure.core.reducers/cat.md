## clojure.core.reducers/cat



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1236"><img valign="middle" alt="[+] 0.0-1236" title="Added in 0.0-1236" src="https://img.shields.io/badge/+-0.0--1236-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__cat__)<br>
</samp>
 <samp>
(__cat__ ctor)<br>
</samp>
 <samp>
(__cat__ left right)<br>
</samp>

---





Source docstring:

```
A high-performance combining fn that yields the catenation of the
reduced values. The result is reducible, foldable, seqable and
counted, providing the identity collections are reducible, seqable
and counted. The single argument version will build a combining fn
with the supplied identity constructor. Tests for identity
with (zero? (count x)). See also foldcat.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/clojure/core/reducers.cljs#L204-L221):

```clj
(defn cat
  ([] (array))
  ([ctor]
     (fn
       ([] (ctor))
       ([left right] (cat left right))))
  ([left right]
     (cond
       (zero? (count left)) right
       (zero? (count right)) left
       :else
       (Cat. (+ (count left) (count right)) left right))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1236
└── src
    └── cljs
        └── clojure
            └── core
                └── <ins>[reducers.cljs:204-221](https://github.com/clojure/clojurescript/blob/r1236/src/cljs/clojure/core/reducers.cljs#L204-L221)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core.reducers/cat` @ crossclj](http://crossclj.info/fun/clojure.core.reducers.cljs/cat.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.core.reducers/cat.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.core.reducers",
 :name "cat",
 :signature ["[]" "[ctor]" "[left right]"],
 :history [["+" "0.0-1236"]],
 :type "function",
 :full-name-encode "clojure.core.reducers/cat",
 :source {:code "(defn cat\n  ([] (array))\n  ([ctor]\n     (fn\n       ([] (ctor))\n       ([left right] (cat left right))))\n  ([left right]\n     (cond\n       (zero? (count left)) right\n       (zero? (count right)) left\n       :else\n       (Cat. (+ (count left) (count right)) left right))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1236",
          :filename "src/cljs/clojure/core/reducers.cljs",
          :lines [204 221]},
 :full-name "clojure.core.reducers/cat",
 :docstring "A high-performance combining fn that yields the catenation of the\nreduced values. The result is reducible, foldable, seqable and\ncounted, providing the identity collections are reducible, seqable\nand counted. The single argument version will build a combining fn\nwith the supplied identity constructor. Tests for identity\nwith (zero? (count x)). See also foldcat."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.core.reducers/cat"]))
```

-->