## ~~cljs.core/HashMap.EMPTY~~



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> <a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[×] 0.0-1798" title="Removed in 0.0-1798" src="https://img.shields.io/badge/×-0.0--1798-red.svg"></a> </td>
</tr>
</table>









Source code @ [github]():

```clj
(set! cljs.core.HashMap/EMPTY (HashMap. nil 0 (js-obj) 0))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.core/HashMap.EMPTY` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/HashMap.EMPTY.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/HashMapDOTEMPTY.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "HashMap.EMPTY",
 :history [["+" "0.0-927"] ["-" "0.0-1798"]],
 :parent-type "HashMap",
 :type "var",
 :full-name-encode "cljs.core/HashMapDOTEMPTY",
 :source {:code "(set! cljs.core.HashMap/EMPTY (HashMap. nil 0 (js-obj) 0))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/cljs/cljs/core.cljs",
          :lines [3830]},
 :full-name "cljs.core/HashMap.EMPTY",
 :removed {:in "0.0-1798", :last-seen "0.0-1586"}}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/HashMap.EMPTY"]))
```

-->