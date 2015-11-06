## cljs.core/set-print-err-fn!



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__set-print-err-fn!__ f)<br>
</samp>

---





Source docstring:

```
Set *print-err-fn* to f.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L62-L64):

```clj
(defn set-print-err-fn!
  [f] (set! *print-err-fn* f))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.48
└── src
    └── main
        └── cljs
            └── cljs
                └── <ins>[core.cljs:62-64](https://github.com/clojure/clojurescript/blob/r1.7.48/src/main/cljs/cljs/core.cljs#L62-L64)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/set-print-err-fn!` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/set-print-err-fn%21.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/set-print-err-fnBANG.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "set-print-err-fn!",
 :signature ["[f]"],
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.core/set-print-err-fnBANG",
 :source {:code "(defn set-print-err-fn!\n  [f] (set! *print-err-fn* f))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.48",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [62 64]},
 :full-name "cljs.core/set-print-err-fn!",
 :docstring "Set *print-err-fn* to f."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/set-print-err-fn!"]))
```

-->