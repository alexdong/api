## cljs.core/print-meta?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>

<samp>(print-meta? opts obj)</samp><br>

---

 <samp>
(__print-meta?__ opts obj)<br>
</samp>

---







Source code @ [github]():

```clj
(defn ^boolean print-meta? [opts obj]
  (and (boolean (get opts :meta))
       (implements? IMeta obj)
       (not (nil? (meta obj)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.core/print-meta?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/print-meta%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/print-metaQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type boolean,
 :ns "cljs.core",
 :name "print-meta?",
 :signature ["[opts obj]"],
 :name-encode "print-metaQMARK",
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.core/print-metaQMARK",
 :source {:code "(defn ^boolean print-meta? [opts obj]\n  (and (boolean (get opts :meta))\n       (implements? IMeta obj)\n       (not (nil? (meta obj)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.8.51",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [9036 9039],
          :url "https://github.com/clojure/clojurescript/blob/r1.8.51/src/main/cljs/cljs/core.cljs#L9036-L9039"},
 :usage ["(print-meta? opts obj)"],
 :full-name "cljs.core/print-meta?",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/print-metaQMARK.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/print-meta?"]))
```

-->