## ~~cljs.core/pr-sequential~~



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> <a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1798"><img valign="middle" alt="[×] 0.0-1798" title="Removed in 0.0-1798" src="https://img.shields.io/badge/×-0.0--1798-red.svg"></a> </td>
</tr>
</table>

<samp>(pr-sequential print-one begin sep end opts coll)</samp><br>

---

 <samp>
(__pr-sequential__ print-one begin sep end opts coll)<br>
</samp>

---





Source docstring:

```
Do not use this.  It is kept for backwards compatibility with the
old IPrintable protocol.
```


Source code @ [github]():

```clj
(defn ^:deprecated pr-sequential
  [print-one begin sep end opts coll]
  (concat [begin]
          (flatten1
            (interpose [sep] (map #(print-one % opts) coll)))
          [end]))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.core/pr-sequential` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/pr-sequential.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/pr-sequential.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "pr-sequential",
 :signature ["[print-one begin sep end opts coll]"],
 :history [["+" "0.0-927"] ["-" "0.0-1798"]],
 :type "function",
 :full-name-encode "cljs.core/pr-sequential",
 :source {:code "(defn ^:deprecated pr-sequential\n  [print-one begin sep end opts coll]\n  (concat [begin]\n          (flatten1\n            (interpose [sep] (map #(print-one % opts) coll)))\n          [end]))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1586",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6210 6217]},
 :usage ["(pr-sequential print-one begin sep end opts coll)"],
 :full-name "cljs.core/pr-sequential",
 :docstring "Do not use this.  It is kept for backwards compatibility with the\nold IPrintable protocol.",
 :removed {:in "0.0-1798", :last-seen "0.0-1586"}}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/pr-sequential"]))
```

-->