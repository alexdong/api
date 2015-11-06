## cljs.core/PersistentTreeMapSeq



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__PersistentTreeMapSeq.__ meta stack ascending? cnt __hash)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L4351-L4391):

```clj
(deftype PersistentTreeMapSeq [meta stack ascending? cnt ^:mutable __hash]
  Object
  (toString [this]
    (pr-str this))

  ISeqable
  (-seq [this] this)

  ISequential
  ISeq
  (-first [this] (peek stack))

  (-rest [this]
    (let [t (peek stack)
          next-stack (tree-map-seq-push (if ascending? (.-right t) (.-left t))
                                        (pop stack)
                                        ascending?)]
      (if (coercive-not= next-stack nil)
        (PersistentTreeMapSeq. nil next-stack ascending? (dec cnt) nil))))

  ICounted
  (-count [coll]
    (if (neg? cnt)
      (inc (count (next coll)))
      cnt))

  IEquiv
  (-equiv [coll other] (equiv-sequential coll other))

  ICollection
  (-conj [coll o] (cons o coll))

  IHash
  (-hash [coll] (caching-hash coll hash-coll __hash))

  IMeta
  (-meta [coll] meta)

  IWithMeta
  (-with-meta [coll meta]
    (PersistentTreeMapSeq. meta stack ascending? cnt __hash)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1211
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4351-4391](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L4351-L4391)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/PersistentTreeMapSeq` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/PersistentTreeMapSeq.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/PersistentTreeMapSeq.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "PersistentTreeMapSeq",
 :type "type",
 :signature ["[meta stack ascending? cnt __hash]"],
 :source {:code "(deftype PersistentTreeMapSeq [meta stack ascending? cnt ^:mutable __hash]\n  Object\n  (toString [this]\n    (pr-str this))\n\n  ISeqable\n  (-seq [this] this)\n\n  ISequential\n  ISeq\n  (-first [this] (peek stack))\n\n  (-rest [this]\n    (let [t (peek stack)\n          next-stack (tree-map-seq-push (if ascending? (.-right t) (.-left t))\n                                        (pop stack)\n                                        ascending?)]\n      (if (coercive-not= next-stack nil)\n        (PersistentTreeMapSeq. nil next-stack ascending? (dec cnt) nil))))\n\n  ICounted\n  (-count [coll]\n    (if (neg? cnt)\n      (inc (count (next coll)))\n      cnt))\n\n  IEquiv\n  (-equiv [coll other] (equiv-sequential coll other))\n\n  ICollection\n  (-conj [coll o] (cons o coll))\n\n  IHash\n  (-hash [coll] (caching-hash coll hash-coll __hash))\n\n  IMeta\n  (-meta [coll] meta)\n\n  IWithMeta\n  (-with-meta [coll meta]\n    (PersistentTreeMapSeq. meta stack ascending? cnt __hash)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1211",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4351 4391]},
 :full-name "cljs.core/PersistentTreeMapSeq",
 :full-name-encode "cljs.core/PersistentTreeMapSeq",
 :history [["+" "0.0-1211"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/PersistentTreeMapSeq"]))
```

-->