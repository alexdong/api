## cljs.core/disj!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/disj!</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/disj!)
</td>
</tr>
</table>


 <samp>
(__disj!__ tcoll val)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L1739-L1740):

```clj
(defn disj! [tcoll val]
  (-disjoin! tcoll val))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1211
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1739-1740](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L1739-L1740)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/disj!` @ clojuredocs](http://clojuredocs.org/clojure.core/disj!)<br>
[`clojure.core/disj!` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/disj%21/)<br>
[`clojure.core/disj!` @ crossclj](http://crossclj.info/fun/clojure.core/disj%21.html)<br>
[`cljs.core/disj!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/disj%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/disjBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "disj!",
 :signature ["[tcoll val]"],
 :history [["+" "0.0-1211"]],
 :type "function",
 :full-name-encode "cljs.core/disjBANG",
 :source {:code "(defn disj! [tcoll val]\n  (-disjoin! tcoll val))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1211",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1739 1740]},
 :full-name "cljs.core/disj!",
 :clj-symbol "clojure.core/disj!"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/disj!"]))
```

-->