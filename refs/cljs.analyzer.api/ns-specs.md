## ~~cljs.analyzer.api/ns-specs~~



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2629"><img valign="middle" alt="[+] 0.0-2629" title="Added in 0.0-2629" src="https://img.shields.io/badge/+-0.0--2629-lightgrey.svg"></a> <a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2655"><img valign="middle" alt="[×] 0.0-2655" title="Removed in 0.0-2655" src="https://img.shields.io/badge/×-0.0--2655-red.svg"></a> </td>
</tr>
</table>

<samp>(ns-specs ns)</samp><br>

---

 <samp>
(__ns-specs__ ns)<br>
</samp>

---





Source docstring:

```
Given a namespace return all the original specs for a namspace as originally
provided in the source.
```


Source code @ [github]():

```clj
(defn ns-specs
  [ns]
  {:pre [(symbol? ns)]}
  (get-in @env/*compiler* [::ana/namespaces ns :specs]))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.analyzer.api/ns-specs` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/ns-specs.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api/ns-specs.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "ns-specs",
 :signature ["[ns]"],
 :history [["+" "0.0-2629"] ["-" "0.0-2655"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api/ns-specs",
 :source {:code "(defn ns-specs\n  [ns]\n  {:pre [(symbol? ns)]}\n  (get-in @env/*compiler* [::ana/namespaces ns :specs]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2644",
          :filename "src/clj/cljs/analyzer/api.clj",
          :lines [48 53]},
 :usage ["(ns-specs ns)"],
 :full-name "cljs.analyzer.api/ns-specs",
 :docstring "Given a namespace return all the original specs for a namspace as originally\nprovided in the source.",
 :removed {:in "0.0-2655", :last-seen "0.0-2644"}}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/ns-specs"]))
```

-->