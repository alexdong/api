## cljs.core/cond->



 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[+] 0.0-1798" title="Added in 0.0-1798" src="https://img.shields.io/badge/+-0.0--1798-lightgrey.svg"></a> </td>
<td>
imported [<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/cond-></samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/cond->)
</td>
</tr>
</table>

<samp>(cond-> expr & clauses)</samp><br>

---

 <samp>
(__cond->__ expr & clauses)<br>
</samp>

---

Takes an expression and a set of test/form pairs. Threads `expr` (via `->`)
through each form for which the corresponding test expression is true.

Note that, unlike `cond` branching, `cond->` threading does not short circuit
after the first true test expression.



---

###### Examples:

```clj
(def a 12)
(cond-> a
  (> a 10) (str " is greater than 10")
  (< a 20) (str " and less than 20"))
;;=> "12 is greater than 10 and less than 20"
```



---

###### See Also:

[`cljs.core/->`](../cljs.core/-GT.md)<br>
[`cljs.core/->>`](../cljs.core/-GTGT.md)<br>
[`cljs.core/cond->>`](../cljs.core/cond-GTGT.md)<br>
[`cljs.core/cond`](../cljs.core/cond.md)<br>

---


Source docstring:

```
Takes an expression and a set of test/form pairs. Threads expr (via ->)
through each form for which the corresponding test
expression is true. Note that, unlike cond branching, cond-> threading does
not short circuit after the first true test expression.
```


Source code @ [github]():

```clj
(defmacro cond->
  [expr & clauses]
  (assert (even? (count clauses)))
  (let [g (gensym)
        steps (map (fn [[test step]] `(if ~test (-> ~g ~step) ~g))
                   (partition 2 clauses))]
    `(let [~g ~expr
           ~@(interleave (repeat g) (butlast steps))]
       ~(if (empty? steps)
          g
          (last steps)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`clojure.core/cond->` @ clojuredocs](http://clojuredocs.org/clojure.core/cond->)<br>
[`clojure.core/cond->` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/cond-%3E/)<br>
[`clojure.core/cond->` @ crossclj](http://crossclj.info/fun/clojure.core/cond-%3E.html)<br>
[`cljs.core/cond->` @ crossclj](http://crossclj.info/fun/cljs.core/cond-%3E.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/cond-GT.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Takes an expression and a set of test/form pairs. Threads `expr` (via `->`)\nthrough each form for which the corresponding test expression is true.\n\nNote that, unlike `cond` branching, `cond->` threading does not short circuit\nafter the first true test expression.",
 :ns "cljs.core",
 :name "cond->",
 :signature ["[expr & clauses]"],
 :name-encode "cond-GT",
 :history [["+" "0.0-1798"]],
 :type "macro",
 :clj-equiv {:full-name "clojure.core/cond->",
             :url "http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/cond->"},
 :related ["cljs.core/->"
           "cljs.core/->>"
           "cljs.core/cond->>"
           "cljs.core/cond"],
 :full-name-encode "cljs.core/cond-GT",
 :source {:code "(defmacro cond->\n  [expr & clauses]\n  (assert (even? (count clauses)))\n  (let [g (gensym)\n        steps (map (fn [[test step]] `(if ~test (-> ~g ~step) ~g))\n                   (partition 2 clauses))]\n    `(let [~g ~expr\n           ~@(interleave (repeat g) (butlast steps))]\n       ~(if (empty? steps)\n          g\n          (last steps)))))",
          :title "Source code",
          :repo "clojure",
          :tag "clojure-1.8.0",
          :filename "src/clj/clojure/core.clj",
          :lines [7240 7255],
          :url "https://github.com/clojure/clojure/blob/clojure-1.8.0/src/clj/clojure/core.clj#L7240-L7255"},
 :usage ["(cond-> expr & clauses)"],
 :examples [{:id "f08338",
             :content "```clj\n(def a 12)\n(cond-> a\n  (> a 10) (str \" is greater than 10\")\n  (< a 20) (str \" and less than 20\"))\n;;=> \"12 is greater than 10 and less than 20\"\n```"}],
 :full-name "cljs.core/cond->",
 :docstring "Takes an expression and a set of test/form pairs. Threads expr (via ->)\nthrough each form for which the corresponding test\nexpression is true. Note that, unlike cond branching, cond-> threading does\nnot short circuit after the first true test expression.",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/cond-GT.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/cond->"]))
```

-->